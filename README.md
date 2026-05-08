# mi-car-trial

> 灏忕背姹借溅锛圫U7 / YU7 绯诲垪锛夎捶娆捐仛鍚堣瘯绠?Agent Skill

鏍规嵁杞﹀瀷鍚嶃€佹€昏溅浠枫€侀浠橈紙閲戦鎴栨瘮渚嬶級銆佹湡鏁帮紝璋冪敤灏忕背澶╂槦閲戣瀺 `af-portal-api` 鐨勫厤鐧诲綍鑱氬悎璇曠畻鎺ュ彛锛岃繑鍥炴墍鏈夊彲閫変骇鍝佹柟妗堝強姣忎釜鏂规鐨勬湀渚涖€佸埄鐜囥€佹墜缁垂銆佹€诲埄鎭瓑璇曠畻缁撴灉銆?
- **鍙椾紬**锛氬皬绫虫苯杞︽綔鍦ㄨ溅涓?/ 閿€鍞【闂?/ 閲戣瀺鏂规璇勪及
- **閫傞厤杞﹀瀷**锛氬皬绫?SU7 / SU7 Pro / SU7 Max / SU7 Ultra / YU7 绯诲垪
- **涓嶉€傜敤**锛氬皬楣?/ 钄氭潵 / 鐞嗘兂 / 鐗规柉鎷夌瓑鍏朵粬鍝佺墝

---

## 鈿狅笍 鍏嶈矗澹版槑

- 鏈?Skill 涓?*闈炲畼鏂瑰伐鍏?*锛屼粎渚涚爺绌躲€佷釜浜鸿喘杞︽祴绠椾娇鐢紱鎵€鏈夐噾铻嶆柟妗堜笌鏁版嵁**浠ュ皬绫冲ぉ鏄熼噾铻嶅畼鏂规笭閬擄紙App / 瀹樼綉 / 闂ㄥ簵锛夊叕绀轰负鍑?*銆?- Skill 鐩存帴璋冪敤灏忕背澶╂槦閲戣瀺鍏紑鎺ュ彛 `https://afs.airstarfinance.net/api/`锛?*涓嶄繚璇佹帴鍙ｉ暱鏈熺ǔ瀹?*锛屾帴鍙ｅ彉鏇淬€侀檺娴併€佷笅绾垮潎鍙兘瀵艰嚧 Skill 澶辨晥銆?- 璇曠畻缁撴灉**浠呬负鍙傝€?*锛屾渶缁堟斁娆惧埄鐜囥€佹湡鏁般€侀浠樻瘮渚嬬敱閲戣瀺鏈烘瀯椋庢帶瀹℃壒鍐冲畾銆?- 璇峰嬁灏嗘湰宸ュ叿鐢ㄤ簬瀵瑰閲戣瀺閿€鍞€佷唬瀹㈠喅绛栫瓑鍦烘櫙锛岀敱姝や骇鐢熺殑涓€鍒囧悗鏋滀笌鏈?Skill 浣滆€呮棤鍏炽€?
---

## 瀹夎

### 鏂瑰紡 1锛氶€氳繃 skills.sh锛堟帹鑽?Claude Code / OpenCode / Cursor 鐢ㄦ埛锛?
```bash
npx skills add caojia321/mi-car-trial
```

### 鏂瑰紡 2锛氶€氳繃 gh skill锛圙itHub CLI Extension锛?
瑕佹眰 `gh >= 2.90.0` 骞跺凡瀹夎 `github/gh-skill` 鎵╁睍锛?
```bash
gh extension install github/gh-skill
gh skill install caojia321/mi-car-trial mi-car-trial --agent opencode
# 鍏朵粬 agent 鍙€夛細claude-code | cursor | codex | gemini | antigravity
```

### 鏂瑰紡 3锛氶€氳繃 ClawHub

```bash
clawhub skill install caojia321/mi-car-trial
```

### 鏂瑰紡 4锛氭墜鍔ㄥ畨瑁?
```bash
git clone https://github.com/caojia321/mi-car-trial.git \
  ~/.config/opencode/skills/mi-car-trial
# 鎴栨斁鍏?~/.claude/skills/ / ~/.agents/skills/ 瀵瑰簲鐩綍
```

### 鐜瑕佹眰

- Python 3.7+
- 浠呬娇鐢?Python 鏍囧噯搴擄紙`urllib` + `json`锛夛紝**鏃?pip 渚濊禆**
- 鍙闂?`https://afs.airstarfinance.net/api`锛堝叕缃戯紝闈炲皬绫冲唴缃戯級

---

## 浣跨敤

瑙﹀彂 Skill 鐨勮嚜鐒惰瑷€鍏抽敭璇嶏細`璇曠畻`銆乣璐锋鏂规`銆乣鑱氬悎璇曠畻`銆乣鎴戞兂涔癭銆乣灏忕背 SU7`銆乣灏忕背 YU7`銆乣璐溅鏂规`銆乣鏈堜緵`銆?
### 绀轰緥瀵硅瘽

> **鐢ㄦ埛**锛氭垜鎯充拱 SU7 Max锛岄《閰?30 涓囷紝棣栦粯 3 鎴愶紝鍒?36 鏈燂紝甯垜绠椾竴涓嬫湀渚?>
> **Agent**锛氾紙鑷姩瑙﹀彂 mi-car-trial Skill锛岃緭鍑烘墍鏈夐€傜敤閲戣瀺浜у搧鐨勬湀渚涘姣旇〃锛?
### CLI 瀛愬懡浠わ紙渚?Agent 璋冪敤锛屼篃鍙嫭绔嬩娇鐢級

Skill 鎻愪緵 6 涓師瀛?CLI 瀛愬懡浠わ紝鍏ュ彛 `python -m scripts.cli <subcommand>`锛?
| 瀛愬懡浠?| 鐢ㄩ€?|
|---|---|
| `terms` | 鍒楀嚭褰撳墠鏀寔鐨勬湡鏁伴€夐」锛?2/24/36/48/60鈥︼級 |
| `car-models` | 鍒楀嚭鏀寔鐨勮溅鍨嬫竻鍗曪紙SU7 鍚勯厤缃?+ YU7 鍚勯厤缃級 |
| `match <杞﹀瀷鍚?` | 妯＄硦鍖归厤鐢ㄦ埛杈撳叆 鈫?鏍囧噯杞﹀瀷 ID |
| `calc-down <鎬讳环> <姣斾緥鎴栭噾棰?` | 璁＄畻棣栦粯閲戦 |
| `aggregate <杞﹀瀷> <鎬讳环> <棣栦粯> <鏈熸暟>` | 璋冪敤鑱氬悎璇曠畻鎺ュ彛锛岃繑鍥炴墍鏈夊彲閫夋柟妗?|
| `evaluate <aggregate 杈撳嚭>` | 瀵规柟妗堟帓搴忋€佹寫閫夋帹鑽愮粍鍚堛€佽緭鍑轰汉绫诲彲璇绘憳瑕?|

瀹屾暣鍙傛暟鍙傝€?`scripts/cli.py`銆?
### 鍏稿瀷璋冪敤閾撅紙Agent 鍐呴儴锛?
```
鐢ㄦ埛鑷劧璇█
  鈫?match (杞﹀瀷褰掍竴鍖?
  鈫?calc-down (棣栦粯閲戦鎹㈢畻)
  鈫?aggregate (鑱氬悎璇曠畻 HTTP 璋冪敤)
  鈫?evaluate (鎵撳垎 & 鎽樿)
  鈫?杈撳嚭缁欑敤鎴?```

---

## 鐩綍缁撴瀯

```
mi-car-trial/
鈹溾攢鈹€ SKILL.md                   # Skill 鍏冧俊鎭?+ 浣跨敤璇存槑锛圓gent 棣栬鏂囦欢锛?鈹溾攢鈹€ README.md                  # 鏈枃浠?鈹溾攢鈹€ LICENSE                    # MIT
鈹溾攢鈹€ .gitignore
鈹溾攢鈹€ CHANGELOG.md               # 鐗堟湰璁板綍
鈹斺攢鈹€ scripts/
    鈹溾攢鈹€ cli.py                 # 缁熶竴 CLI 鍏ュ彛
    鈹斺攢鈹€ core/
        鈹溾攢鈹€ http.py            # 涓?afs.airstarfinance.net 鐨?HTTP 瀹㈡埛绔?        鈹溾攢鈹€ aggregate.py       # 鑱氬悎璇曠畻鎺ュ彛灏佽
        鈹溾攢鈹€ car_models.py      # 杞﹀瀷娓呭崟 + 妯＄硦鍖归厤
        鈹溾攢鈹€ terms.py           # 鏈熸暟瀹氫箟
        鈹溾攢鈹€ money.py           # 棣栦粯閲戦/姣斾緥鎹㈢畻銆侀噾棰濇牸寮忓寲
        鈹斺攢鈹€ evaluate.py        # 鏂规鎵撳垎涓庢憳瑕?```

---

## 鏁呴殰鎺掓煡

### `HTTPError 403` / 鎺ュ彛琚嫆

鎺ュ彛鍙兘宸叉洿鏂伴鎺х瓥鐣ャ€備紭鍏堜粠 SU7 App 瀹樻柟绔鐜伴棶棰樺苟纭鍏紑鎺ュ彛鏄惁鍙樻洿銆?
### `ConnectionError` / 璇锋眰瓒呮椂

纭鏈満鍙互 ping / 璁块棶 `afs.airstarfinance.net`銆備釜鍒唬鐞?VPN 浼氭嫤鎴鍩熷悕銆?
### 杩斿洖鏂规涓虹┖

- 妫€鏌ヨ溅鍨嬫槸鍚﹀湪 `python -m scripts.cli car-models` 娓呭崟涓?- 妫€鏌ユ湡鏁版槸鍚﹀湪 `python -m scripts.cli terms` 鏀寔鑼冨洿
- 纭棣栦粯姣斾緥鏄惁鍦ㄩ噾铻嶄骇鍝佸悎瑙勫尯闂达紙閫氬父 20%鈥?0%锛?
### Skill 娌¤ Agent 瑙﹀彂

- 妫€鏌?`SKILL.md` 鐨?`description` 鏄惁鍖呭惈瑙﹀彂璇?- 閲嶅惎 agent host锛圕laude Code / OpenCode 绛夛級璁╁叾閲嶆柊绱㈠紩 skills 鐩綍
- 纭 Skill 宸插畨瑁呭埌瀵瑰簲 agent 鐨勬壂鎻忚矾寰勶紙`~/.config/opencode/skills/` 鎴?`~/.claude/skills/` 绛夛級

---

## 璐＄尞

娆㈣繋 issue / PR銆傛柊澧炶溅鍨嬫垨閫傞厤鏂颁骇鍝佹椂锛?
1. 鍦?`scripts/core/car_models.py` 杩藉姞鏉＄洰
2. 鍦?`scripts/core/terms.py` 纭鏈熸暟
3. 杩愯 `python -m scripts.cli aggregate ...` 楠岃瘉杩斿洖
4. 鏇存柊 `CHANGELOG.md`

---

## License

[MIT](./LICENSE) 漏 2026 澶╂槦鏁扮绉戞妧鏈夐檺鍏徃 (Xiaomi Finance / Airstar Finance)
