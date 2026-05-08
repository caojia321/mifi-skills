---
name: mi-car-trial
description: 鏍规嵁鐢ㄦ埛鎻忚堪锛堣溅鍨嬪悕銆佹€昏溅浠枫€侀浠橀噾棰濇垨棣栦粯姣斾緥銆佹湡鏁帮級锛岃皟鐢ㄥ皬绫冲ぉ鏄熼噾铻?af-portal-api 鐨勫厤鐧诲綍鑱氬悎璇曠畻鎺ュ彛锛岃繑鍥炴墍鏈夊彲閫変骇鍝佹柟妗堝強姣忎釜鏂规鐨勮瘯绠楃粨鏋溿€傛湰鎶€鑳戒粎閫傜敤浜?*灏忕背姹借溅**锛堝皬绫?SU7 / SU7 Pro / SU7 Max / SU7 Ultra / YU7 绛夌郴鍒楋級锛?*涓嶉€傜敤浜庡皬楣?/ 钄氭潵 / 鐞嗘兂绛夊叾浠栧搧鐗?*銆傝Е鍙戣瘝锛氳瘯绠椼€佽捶娆炬柟妗堛€佽仛鍚堣瘯绠椼€佹垜鎯充拱銆佸皬绫砈U7銆佸皬绫砓U7銆佽喘杞︽柟妗堛€佹湀渚涖€?license: MIT
compatibility:
  - claude-code
  - opencode
  - cursor
  - copilot
  - codex
  - gemini
metadata:
  author: 澶╂槦鏁扮绉戞妧鏈夐檺鍏徃 (Xiaomi Finance / Airstar Finance)
  version: 1.0.0
  homepage: https://github.com/caojia321/mi-car-trial
  repository: https://github.com/caojia321/mi-car-trial
  tags:
    - xiaomi
    - finance
    - car-loan
    - su7
    - yu7
    - chinese
    - cli
  external_costs: 鏃犺垂鐢紱璋冪敤灏忕背澶╂槦閲戣瀺鍏紑鑱氬悎璇曠畻鎺ュ彛 https://afs.airstarfinance.net/api/锛屽彲鑳藉彈闄愭祦鎴栨帴鍙ｅ彉鏇村奖鍝嶃€?---

# Mi Car Trial锛堝皬绫虫苯杞﹁捶娆捐瘯绠楋級

璋冪敤**灏忕背澶╂槦閲戣瀺** 鍏嶇櫥褰曡仛鍚堣瘯绠楁帴鍙ｏ紝鏍规嵁鐢ㄦ埛涓€鍙ヨ瘽闇€姹傦紙濡傘€屾垜鎯充拱涓€杈嗗皬绫?SU7 鏍囧噯鐗堬紝鎬昏溅浠?21.59 涓囷紝棣栦粯 5 涓囷紝鍒?36 鏈熴€嶏級杩斿洖鎵€鏈夊彲鐢ㄤ骇鍝佹柟妗堜笌閫愭柟妗堣瘯绠楃粨鏋溿€?
> **閫傜敤鑼冨洿**锛氭湰鎶€鑳藉彧瑕嗙洊**灏忕背姹借溅**锛圶iaomi锛夊湪鍞殑 SU7 / SU7 Pro / SU7 Max / SU7 Ultra / SU7 Ultra 璧涢亾涓撲笟鏀硅鐗?/ SU7 Ultra 绾藉崥鏍兼灄鐗?/ YU7 / YU7 Pro / YU7 Max / 灏忕背瀹氬埗鐗堢瓑绯诲垪銆傝嫢鐢ㄦ埛璇㈤棶灏忛箯銆佽敋鏉ャ€佺悊鎯炽€佺壒鏂媺銆佹瘮浜氳开绛夊叾浠栧搧鐗岃溅鍨嬶紝**蹇呴』鏄庣‘鍛婄煡鏈妧鑳戒笉鏀寔**锛屼笉寰楀己琛屾妸鍏朵粬鍝佺墝杞﹀瀷鍚嶉€佽繘 `match` 瀛愬懡浠ゃ€?
## 鐩綍缁撴瀯

```text
mi-car-trial/
  SKILL.md
  scripts/
    cli.py          # 缁熶竴 CLI 鍏ュ彛锛堟墍鏈夊閮ㄨ皟鐢ㄥ彧璧板畠锛?    core/           # 绾嚱鏁版牳蹇冧笟鍔★紙HTTP銆侀噾棰濇崲绠椼€佽瘎浼般€佽溅鍨嬪尮閰嶁€︼級
      http.py  money.py  terms.py  car_models.py  aggregate.py  evaluate.py
```

CLI 涓?core 鐨勫垎灞傜害瀹氾細

- `core/*`锛氬彧鎺ュ彈/杩斿洖 Python 瀵硅薄锛屽け璐ユ姏 `MiCarTrialError`锛?*涓嶅仛 print / sys.exit**銆?- `scripts/cli.py`锛氬敮涓€瀵瑰鍙墽琛屽叆鍙ｏ紝璐熻矗鍙傛暟瑙ｆ瀽 + UTF-8 JSON IO + 閫€鍑虹爜銆?- 涓讳細璇?/ 鍏跺畠鑴氭湰 / 鏈潵鐢ㄦ埛鑷繁鐨勫伐鍏凤細**鍙皟 `python scripts/cli.py <瀛愬懡浠?`**锛屼笉鐩存帴 import core銆佷笉鐩存帴鎵撴帴鍙ｃ€?
## 鏍稿績璁捐鍘熷垯锛氫竴鍒囪绠椾笌鎺ュ彛璋冪敤涓嬫矇鍒?CLI

**鏈妧鑳戒弗鏍肩姝㈠湪涓讳細璇濅腑鍋氫互涓嬩簨鎯?*锛?
- **浠讳綍鏁板杩愮畻**锛氬崟浣嶆崲绠楋紙鍏?涓囧厓 鈫?鍒嗭級銆侀浠樻瘮渚?鈫?閲戦銆佹湀渚?璐锋閲戦鎺ㄧ畻銆侀浠樺尯闂村垽鏂€佹湡鏁版敮鎸佹牎楠屸€斺€斿叏閮ㄩ€氳繃 CLI 瀹屾垚銆?- **鎵嬪姩缁勮鎴栬В鏋?HTTP 璇锋眰/鍝嶅簲鐨?JSON**锛氫笉瑕佺敤 `Invoke-RestMethod` / `curl` 鐩存帴璋冩帴鍙ｃ€?- **鍑蹇嗗啓鍑烘敮鎸佹湡鏁?*锛氬繀椤绘瘡娆¤繍琛?`cli.py terms`銆?- **鑲夌溂鎵弿 schemes 绛涘彲鐢ㄦ柟妗?*锛氬繀椤昏蛋 `cli.py evaluate` 鎷跨粨鏋勫寲缁撴灉銆?
涓讳細璇濈殑鑱岃矗鍙湁涓や欢锛?*鈶?鍚戠敤鎴烽棶娓呭弬鏁?鈶?鎸変互涓?"CLI 瀛愬懡浠?鈫?璇?JSON" 鐨勬祦绋嬩覆璧锋潵**銆?
### CLI 瀛愬懡浠ゆ竻鍗?
| 瀛愬懡浠?| 鑱岃矗 | 杈撳叆 | 杈撳嚭锛坰tdout锛?|
|---|---|---|---|
| `terms` | `GET /supported-terms` | 鏃?| `{"terms":[12,24,36,48,60]}` |
| `car-models` | `GET /car-models` | 鏃?| `{"cars":[{carModelId,modelName,totalAmount(鍒?,serialId,serialName},...]}` |
| `match` | `/car-models` + 鍖呭惈鍖归厤锛堝拷鐣ョ┖鏍?澶у皬鍐欙級 | `--name <杞﹀瀷鍚?` | `{"status":"ok"/"multiple"/"none",...}` |
| `calc-down` | 閲戦/姣斾緥 鈫?鍒?鎹㈢畻 | `--yuan` \| `--wan` \| `--vehicleValue --rate/--percent` | `{"fen":<鍒?}` |
| `aggregate` | `POST /aggregate` | `--carModelId --vehicleValue --downPaymentAmount --termNo`锛堝叏閮ㄥ垎/鏁存暟锛?| `ProductTrialAggregateVO` 鐨?`data` 瀵硅薄 |
| `evaluate` | 棣栦粯鑼冨洿 + 鏈熸暟鏀寔 + 杩囨护 + 鍒嗙粍鎺掑簭 | stdin UTF-8 JSON | 鍚?available/downOutOfRange/termUnsupported/both/summary 鐨勭粨鏋?|

鎵€鏈?CLI 璋冪敤锛?
- 鎴愬姛 鈫?exit 0 + stdout 杈撳嚭绱у噾 UTF-8 JSON
- 澶辫触 鈫?exit != 0 + stderr 鎵撳嵃閿欒锛?*涓ョ浣跨敤浠讳綍鏈湴鍏滃簳鍊肩户缁?*
- 璺ㄥ钩鍙?Python 3.7+锛堝彧渚濊禆鏍囧噯搴?urllib + json锛夛紝鏃犻渶 pip 瀹夎

## 瑙﹀彂鏉′欢

婊¤冻浠讳竴鍗冲彲瑙﹀彂锛?
- 鐢ㄦ埛鎻愬埌銆岃瘯绠椼€嶃€岃仛鍚堣瘯绠椼€嶃€岃捶娆炬柟妗堛€嶃€岃喘杞︽柟妗堛€嶃€屾湀渚涖€嶃€屽垎鏈熴€嶏紝**涓?*璇鎸囧悜灏忕背姹借溅
- 鐢ㄦ埛浠ャ€屾垜鎯充拱涓€杈嗏€﹁溅銆嶃€屾煡涓€涓?xxx 杞︾殑璐锋鏂规銆嶇瓑鍙ュ紡鎻忚堪璐溅鎰忓浘锛屽苟鐐瑰悕灏忕背绯昏溅鍨?- 鐢ㄦ埛鏄庣‘鐐瑰悕**灏忕背**杞﹀瀷锛堝 灏忕背 SU7 / SU7 Ultra / 灏忕背 YU7 绛夛級骞跺笇鏈涗及绠楄捶娆?- 浠呭嚭鐜般€孲U7銆嶃€孻U7銆嶇瓑鍨嬪彿鑰屾湭鍐欏搧鐗屾椂锛?*榛樿瑙嗕负灏忕背**锛堣繖涓や釜鍨嬪彿褰撳墠鍙湁灏忕背鍦ㄥ敭锛夛紱浣嗚嫢鐢ㄦ埛鏄庣‘鍐欍€屽皬楣?SU7銆嶇瓑**閿欒鍝佺墝缁勫悎**锛屽簲鍏堢籂姝ｅ苟纭鍏剁湡瀹炴剰鍥?
## 杈撳叆鎶藉彇锛堜粠鐢ㄦ埛鑷劧璇█瑙ｆ瀽锛?
蹇呴』鎶藉彇浠ヤ笅瀛楁锛?
| 瀛楁 | 蹇呭～ | 璇存槑 |
|---|---|---|
| `carModelName` | 鏄?| 杞﹀瀷鍚嶏紙濡?"SU7 鏍囧噯鐗?锛夛紝鐢ㄤ簬閫氳繃 `cli.py match` 鍖归厤 `carModelId` |
| `vehicleValue` | 鍚?| 鎬昏溅浠凤紙**鍒?*锛屾暣鏁帮級銆傜敤鎴锋湭鎻愪緵鏃朵粠 `match` 鐨勫搷搴斿彇 `totalAmount` |
| `downPaymentAmount` | **鏈€缁堝繀濉?* | 棣栦粯閲戦锛?*鍒?*锛屾暣鏁帮級銆傜敤鎴蜂互姣斾緥/鍏?涓囧厓琛ㄨ揪鏃讹紝璋冪敤 `cli.py calc-down` 鎹㈢畻 |
| `termNo` | 鏄?| 鍒嗘湡鏈熸暟銆?*浼犳暣鏁帮紙濡?12銆?4銆?6銆?8銆?0锛?*锛屼笉瑕佷紶 `TERM_36` 杩欑瀛楃涓?|

### 瑙勫垯

1. **鑱氬悎璇曠畻鎺ュ彛鍙帴鍙楅浠橀噾棰?*锛堝崟浣嶏細鍒嗭級銆傛瘮渚?鍏?涓囧厓涓€寰嬬粡 `cli.py calc-down` 鎹㈢畻涓哄垎鍚庡啀浼犮€?2. **涓嶈鍦ㄤ富浼氳瘽閲屾墜绠?*銆傚嵆渚挎槸"5 涓囧厓 = 5000000 鍒?杩欑鐪嬭捣鏉ョ畝鍗曠殑鎹㈢畻锛屼篃蹇呴』璧?`cli.py calc-down --yuan 50000`锛屼互閬垮厤鍙ｇ畻閿欒鍜屽崟浣嶆贩娣嗐€?3. **鎹㈢畻閫忔槑鎬?*锛欳LI 鎹㈢畻鍚庯紝鍚戠敤鎴风畝瑕佽鏄庯紙渚嬪"鎸?25% 脳 25.35 涓囷紝CLI 璁＄畻棣栦粯 63,375 鍏?锛夛紝閬垮厤鐢ㄦ埛浠ヤ负鎺ュ彛鐩存帴鏀朵簡姣斾緥銆?4. **閲戦鍗曚綅鏄€屽垎銆?*锛欳LI 璇诲啓涓€寰嬬敤鍒嗐€傚睍绀虹粰鐢ㄦ埛鏃跺啀闄や互 100 杞厓銆?5. **鏈熸暟**浼?`int` 鏁板瓧銆傚悗绔?`TermNoEnum` 鐢?`@JsonValue` 搴忓垪鍖栦负鏁板瓧 code锛屼紶 `"TERM_36"` 浼氭姤 `NumberFormatException`銆?6. 鑻ョ敤鎴锋彁渚涖€岃捶娆鹃噾棰濄€嶈€岄潪棣栦粯锛屽憡鐭ユ殏涓嶆敮鎸侊紝璇㈤棶鏀圭敤棣栦粯閲戦鎴栭浠樻瘮渚嬨€?
### 淇℃伅涓嶅叏鏃讹細闂瓟寮忔敹闆?
濡傛灉鐢ㄦ埛棣栨杈撳叆缂哄皯浠讳綍蹇呭～瀛楁锛?*涓嶈鍋囪榛樿鍊?*銆?*涓嶈涓€娆￠棶涓€鍫嗛棶棰?*锛屾寜浠ヤ笅椤哄簭閫愰」杩介棶锛堟瘡娆″彧闂?1 涓級锛?
1. **缂?`carModelName`** 鈫?闂細銆岃闂偍鎯宠瘯绠楀摢娆?*灏忕背姹借溅**锛燂紙濡?灏忕背 SU7 / SU7 Pro / SU7 Max / YU7 / SU7 Ultra 绛夛級銆?2. **缂洪浠?* 鈫?闂細銆岃闂寜棣栦粯閲戦锛堝 5 涓囷級杩樻槸鎸夐浠樻瘮渚嬶紙濡?30%锛夎瘯绠楋紵銆?3. **缂?`termNo`** 鈫?**鍏堣繍琛?* `python scripts/cli.py terms` 鎷垮埌 `terms` 鏁扮粍锛岀劧鍚庢寜杩斿洖椤哄簭鍚戠敤鎴峰睍绀哄€欓€夛細銆岃闂垎鏈熷灏戞湡锛燂紙褰撳墠鏀寔锛歿terms 鎷兼帴锛屽 12 / 24 / 36 / 48 / 60}锛夈€嶃€侰LI 澶辫触锛堥潪 0 閫€鍑猴級鈫?**鍘熸牱鎶ラ敊骞剁粓姝㈡祦绋?*锛屼笉寰楄嚜琛岀寽鏈熸暟銆?4. **涓や釜棣栦粯瀛楁閮界粰浜?*锛堝悓鏃剁粰浜嗛噾棰濆拰姣斾緥锛?鈫?闂細銆屾偍鍚屾椂缁欎簡棣栦粯閲戦鍜岄浠樻瘮渚嬶紝鍙兘浜岄€変竴锛屼繚鐣欏摢涓紵銆?
姣忔鐢ㄦ埛鍥炵瓟鍚庯紝閲嶆柊妫€鏌ュ墿浣欑己澶卞瓧娈碉細鏈夌己 鈫?缁х画闂紱榻愬叏 鈫?杩涘叆璋冪敤娴佺▼銆?
`vehicleValue` 濮嬬粓鍙€夛紝涓嶉渶瑕佷富鍔ㄩ棶銆傜己鐪佹椂璧?Step B 鐨?`cli.py match` 鑷姩鎷垮埌 `totalAmount` 鍚庣洿鎺ョ敤銆?
## 鐜

- **鎵€灞炲叕鍙?*锛氬皬绫冲ぉ鏄熼噾铻嶏紙airstarfinance锛屽皬绫抽泦鍥㈤噾铻嶆澘鍧楋級
- **Base URL**锛歚https://afs.airstarfinance.net/api`
- 鎵€鏈夋帴鍙ｅ潎鍏嶇櫥褰曪紙鏃犻渶閴存潈澶达級銆?- 璇ユ帴鍙ｅ彧杩斿洖**灏忕背姹借溅**鐨勮溅鍨嬩笌閲戣瀺鏂规锛屼笉娑夊強鍏朵粬鍝佺墝銆?- CLI 鍐呴儴缁熶竴鐢?UTF-8 缂栬В鐮侊紝涓嶉渶瑕佸湪涓讳細璇濋噷澶勭悊 `Console.OutputEncoding`銆乣chcp 65001` 绛夌粓绔紪鐮侀棶棰樸€?
## 璋冪敤娴佺▼

> **绾﹀畾**锛氫笅鏂囨墍鏈?`python scripts/cli.py ...` 鍛戒护閮藉湪鏈妧鑳?base directory 涓嬫墽琛屻€傚疄闄呰皟鐢ㄦ椂鐢ㄧ粷瀵硅矾寰?`python <skill-base>/scripts/cli.py ...`銆俉indows 鍙敼鐢?`py scripts/cli.py ...`銆?
### Step A锛氬噯澶囧弬鏁?
#### A.1 鑻ョ敤鎴风敤銆岄浠樻瘮渚嬨€嶈〃杈?鈫?鍏堟崲绠椾负閲戦

闇€瑕佺煡閬?`vehicleValue`锛堝垎锛夋墠鑳芥崲绠楋紝鍥犳鍏堝仛 Step B 鎷垮埌 `totalAmount` 鍐嶅洖鏉ュ仛 A.1锛涙垨鐩存帴鍦?A.2 涔嬪悗鎵ц銆?
```
# 姣斾緥锛堢櫨鍒嗘暟锛?python scripts/cli.py calc-down --vehicleValue 21990000 --percent 30
# 鎴栧皬鏁?python scripts/cli.py calc-down --vehicleValue 21990000 --rate 0.3
# 杈撳嚭锛歿"fen":6597000}
```

#### A.2 鑻ョ敤鎴风敤銆屽厓 / 涓囧厓銆嶈〃杈鹃噾棰?鈫?鎹㈢畻涓哄垎

```
python scripts/cli.py calc-down --yuan 50000     # 5 涓囧厓 鈫?{"fen":5000000}
python scripts/cli.py calc-down --wan 21.99      # 21.99 涓囧厓 鈫?{"fen":21990000}
```

### Step B锛氬尮閰嶈溅鍨嬶紙寰楀埌 carModelId 鍜?vehicleValue锛?
```
python scripts/cli.py match --name "SU7 鏍囧噯鐗?
```

CLI 鍐呴儴鑷姩 `GET /car-models` 骞跺仛**蹇界暐绌烘牸/澶у皬鍐欑殑鍖呭惈鍖归厤**銆傚彲鑳界殑杩斿洖锛?
- `{"status":"ok","car":{carModelId,modelName,totalAmount,...}}` 鈫?鍞竴鍛戒腑锛屽彇鍏?`carModelId` 鍜?`totalAmount`锛堝悗鑰呬綔涓?`vehicleValue`锛夈€?- `{"status":"multiple","candidates":[...]}` 鈫?澶氭潯鍛戒腑锛屽悜鐢ㄦ埛灞曠ず `candidates[].modelName` 璁╁叾鎸戦€夛紱鍐嶇敤 `carModelId` 鐩存帴杩涘叆 Step C锛堟湰娆′細璇濆凡鎸佹湁瀹屾暣鍒楄〃锛屾棤闇€閲嶅鏌ワ級銆?- `{"status":"none","availableModelNames":[...]}` 鈫?闆跺懡涓紝鍛婄煡鐢ㄦ埛骞跺垪鍑?`availableModelNames`銆?
> 娉ㄦ剰锛氳溅鍨嬪悕涓?`"SU7"` / `"SU7 Pro"` / `"SU7 Max"` / `"SU7 Ultra"` 绛夛紝娌℃湁 `"SU7 鏍囧噯鐗?` 杩欑瀛楁牱銆傜敤鎴疯"鏍囧噯鐗?鏃舵槧灏勫埌 `modelName=="SU7"`锛堟渶鍩虹鐗堟湰锛夈€?>
> 鐢ㄦ埛鍙銆孲U7銆嶄細鍖归厤鍒板涓紙SU7銆丼U7 Pro銆丼U7 Max銆丼U7 Ultra鈥︹€﹂兘鍖呭惈"SU7"锛夛紝灞炰簬 `status=multiple`锛岄渶瑕佽鐢ㄦ埛杩涗竴姝ユ槑纭€?
### Step C锛氭彁浜よ仛鍚堣瘯绠?
```
python scripts/cli.py aggregate \
  --carModelId 600046406 \
  --vehicleValue 21990000 \
  --downPaymentAmount 5000000 \
  --termNo 36
```

stdout 鏄?`ProductTrialAggregateVO` 鐨?`data` 瀵硅薄锛岀粨鏋勮涓嬫枃銆?
**娉ㄦ剰**锛?
- **鍙厑璁?`downPaymentAmount`**銆傜姝紶 `downPaymentRate`锛堝嵆渚垮悗绔粨鏋勪綋閲屽彲鑳藉瓨鍦ㄨ瀛楁锛屽湪褰撳墠鐜鐨勮В鏋?鍗曚綅绾﹀畾涓庨鏈熶笉绗︼紝浼氬鑷撮浠樿璇垽涓烘瀬灏忓€硷紝璐锋閲戦寮傚父鏀惧ぇ锛夈€?- `termNo` 蹇呴』鏄?*鏁存暟**锛堝 `36`锛夈€?- 鎵€鏈夐噾棰濆瓧娈靛崟浣嶆槸**鍒?*銆?
### Step D锛氳瘎浼版柟妗堬紙棣栦粯鑼冨洿 + 鏈熸暟鏀寔 + 杩囨护 + 鎺掑簭锛?
**绂佹涓讳細璇濊倝鐪奸亶鍘?`schemes[]` 鍋氫互涓嬪垽鏂?*锛氶浠樻槸鍚﹀湪鑼冨洿鍐呫€佹湡鏁版槸鍚︽敮鎸併€乣calculate == null` 鏄惁璇ヨ繃婊ゃ€佹湀渚涙帓搴忊€斺€斿繀椤讳氦缁?`cli.py evaluate`銆?
```python
# 鎺ㄨ崘锛氶€氳繃 Python 杩涚▼绠￠亾璋冪敤锛堣法骞冲彴銆乁TF-8 骞插噣锛?import json, subprocess

# 1) POST /aggregate
agg_raw = subprocess.check_output([
    "python", "scripts/cli.py", "aggregate",
    "--carModelId", "600046406",
    "--vehicleValue", "21990000",
    "--downPaymentAmount", "5000000",
    "--termNo", "36",
])
aggregate = json.loads(agg_raw.decode("utf-8"))

# 2) 浜ょ粰 evaluate 瀛愬懡浠ゅ鐞?payload = json.dumps({
    "aggregate": aggregate,
    "userDownAmount": 5000000,
    "termNo": 36,
    "vehicleValue": 21990000,
}, ensure_ascii=False).encode("utf-8")

result_raw = subprocess.check_output(
    ["python", "scripts/cli.py", "evaluate"],
    input=payload,
)
result = json.loads(result_raw.decode("utf-8"))
# result.keys() = available / downOutOfRange / termUnsupported / both / filtered / summary
```

> **閲嶈**锛氬繀椤荤敤**瀛楄妭娴佺閬?+ 鏄惧紡 UTF-8 瑙ｇ爜**锛堝涓婄ず渚嬶級銆俉indows Python 鐨?`sys.stdin` 榛樿缂栫爜涓嶆槸 UTF-8锛岀洿鎺ヤ紶瀛楃涓茬閬撲細鎶婁腑鏂囩牬鍧忔垚浠ｇ悊瀛楃銆?>
> 濡傛灉涓€瀹氳鍦?PowerShell / bash 鍛戒护琛岄噷璺戯紝鍙淇濊瘉 `cli.py evaluate` 鐨?stdin 鏄?UTF-8 瀛楄妭娴佸嵆鍙紙CLI 宸插己鍒舵寜 UTF-8 瑙ｇ爜 stdin锛夈€傜ず渚嬶紙bash锛夛細
>
> ```bash
> python scripts/cli.py aggregate --carModelId 600046406 --vehicleValue 21990000 --downPaymentAmount 5000000 --termNo 36 \
>   | python -c "import json,sys; agg=json.load(sys.stdin); print(json.dumps({'aggregate':agg,'userDownAmount':5000000,'termNo':36,'vehicleValue':21990000},ensure_ascii=False))" \
>   | python scripts/cli.py evaluate
> ```

### evaluate 杈撳嚭缁撴瀯

```json
{
  "available":      [<enriched scheme>, ...],
  "downOutOfRange": [<enriched scheme>, ...],
  "termUnsupported":[<enriched scheme>, ...],
  "both":           [<enriched scheme>, ...],
  "filtered":       [<enriched scheme>, ...],
  "summary": {
    "availableCount": 2,
    "downOutOfRangeCount": 1,
    "termUnsupportedCount": 0,
    "bothCount": 0,
    "filteredCount": 0,
    "recommended": {"productTypeName":"鏍囧噯浜у搧","customerName":"闄愭椂7骞翠綆鎭疊","monthlyPayment":501677}
  }
}
```

enriched scheme = 鍘熷 scheme + 涓変釜鏈湴璁＄畻瀛楁锛?- `minAmount` / `maxAmount`锛堝垎锛屽彲鑳戒负 null锛夆€斺€擟LI 鎸?`downInfo.amount` / `downInfo.rate 脳 vehicleValue 梅 10_000_000` 鎺ㄧ畻锛坮ate 鍗曚綅鏄?*鐧句竾鍒嗘瘮**锛歚4600000` = 46%锛?- `downPaymentSupported`锛坆ool锛宒ownInfo 涓?null 鏃惰涓?true锛?- `termSupportedResolved`锛坆ool锛岀患鍚?`termSupported` 瀛楁涓?`supportedTerms` 鍒楄〃锛?
### ProductTrialAggregateVO 鍘熷缁撴瀯锛堜粎渚涘弬鑰冿紝涓嶉渶瑕佷富浼氳瘽瑙ｆ瀽锛?
```json
{
  "carModelId": 600046406,
  "vehicleValue": 21990000,
  "termNo": "36",
  "downPaymentAmount": 5000000,
  "hasFinancialScheme": true,
  "schemes": [
    {
      "productTypeName": "鏍囧噯浜у搧",
      "productSnapshotId": "...",
      "customerName": "闄愭椂7骞翠綆鎭疉",
      "description": "棣栦粯9.99涓囧厓璧凤紝骞村寲璐圭巼1.9%",
      "marketingTag": "浼樻儬",
      "supportedTerms": ["12","24","36","48","60","72","84"],
      "downInfo": {"rate": 4600000, "maxRate": 8500000, "amount": 9990000, "maxAmount": 18691500, "byAmount": true},
      "termSupported": true,
      "calculate": {"monthlyPayment": 498845, "loanAmount": 16990000, "totalInterest": 968436, ...},
      "calculateError": null
    }
  ]
}
```

鑻?`data.hasFinancialScheme == false` 涓?`schemes == []`锛氬憡鐭ョ敤鎴疯杞﹀瀷褰撳墠鏃犲彲鐢ㄩ噾铻嶆柟妗堛€?
## 杈撳嚭缁欑敤鎴?
浠?Markdown 琛ㄦ牸灞曠ず `cli.py evaluate` 杩斿洖鐨?`available + downOutOfRange + termUnsupported + both`锛堟寜璇ラ『搴忓垎缁勶級锛屽叧閿垪锛?
| 浜у搧鍚?| 绫诲瀷 | 鏈堜緵 | 璐锋閲戦 | 鎬诲埄鎭?| 棣栦粯鏀寔鑼冨洿 | 鐘舵€?| 钀ラ攢鏍囩 |
|---|---|---|---|---|---|---|---|

**灞曠ず鏃舵妸鎵€鏈夐噾棰濆瓧娈甸櫎浠?100 杞厓**锛屽繀瑕佹椂鍐嶆崲绠椾负涓囧厓銆備互涓嬫槸**瀛楁绾х殑灞曠ず瑙勫垯**锛屼弗鏍兼寜 evaluate 缁撴灉瀛楁缁勮锛屼笉瑕佹墜鍔ㄤ簩娆¤绠椾换浣曟暟鍊硷細

### 銆岄浠樻敮鎸佽寖鍥淬€嶅垪

- 鍙?enriched scheme 鐨?`minAmount` / `maxAmount`锛圕LI 宸叉帹绠楀ソ锛屽崟浣嶅垎锛?- 涓ょ闄や互 100 灞曠ず鍏?涓囧厓锛屼緥濡?`3涓?- 15涓嘸
- `downPaymentSupported == false` 鈫?鍦ㄨ寖鍥村墠鍔?鈿狅笍 骞舵爣绮楋紝渚嬪 `鈿狅笍 **9.99涓?- 18.69涓囷紙褰撳墠棣栦粯 5 涓囦綆浜庝笅闄愶級**`
- `minAmount == null && maxAmount == null` 鈫?鏄剧ず `鈥擿

### 銆屾湀渚?/ 璐锋閲戦 / 鎬诲埄鎭€嶅垪

- `calculate != null` 鈫?鍒嗗埆鍙?`calculate.monthlyPayment` / `calculate.loanAmount` / `calculate.totalInterest`锛岄櫎浠?100 灞曠ず
- `calculate == null`锛堝嵆 termUnsupported 鎴?both 鍒嗙粍锛夆啋 杩欎笁鍒楃粺涓€鏄剧ず `鈥擿

### 銆岀姸鎬併€嶅垪

- `available` 鈫?鉁?鍙敤
- `downOutOfRange` 鈫?鈿狅笍 棣栦粯瓒呴檺
- `termUnsupported` 鈫?鈿狅笍 鏈熸暟涓嶆敮鎸侊紙鏀寔锛歿supportedTerms 鎷兼帴}锛?- `both` 鈫?鈿狅笍 鏈熸暟涓嶆敮鎸?+ 棣栦粯瓒呴檺

### 琛ㄦ牸涓嬫柟杩藉姞鎻愮ず

- 鑻?`downOutOfRangeCount > 0`锛?  > 鈿狅笍 **浠ヤ笅鏂规褰撳墠棣栦粯涓嶅湪鏀寔鑼冨洿鍐?*锛?  > - {customerName}锛氭敮鎸侀浠?{minAmount/100} - {maxAmount/100} 鍏冿紝褰撳墠棣栦粯 {userDownAmount/100} 鍏?  >
  > 濡傞渶浣跨敤涓婅堪鏂规锛岃璋冩暣棣栦粯閲戦鑷冲搴斿尯闂淬€?
- 鑻?`termUnsupportedCount > 0`锛?  > 鈴憋笍 **浠ヤ笅鏂规涓嶆敮鎸佸綋鍓嶆湡鏁帮紙{termNo} 鏈燂級**锛?  > - {customerName}锛氭敮鎸佹湡鏁?{supportedTerms 鎷兼帴}
  >
  > 濡傞渶浣跨敤涓婅堪鏂规锛岃璋冩暣鏈熸暟鑷冲叾鏀寔鑼冨洿鍐呫€?
- 鎬荤粨锛氥€屽叡 {availableCount} 涓彲鐢ㄦ柟妗堬紙鍏朵腑 {downOutOfRangeCount} 涓洜棣栦粯瓒呴檺闇€璋冩暣锛寋termUnsupportedCount} 涓洜鏈熸暟涓嶆敮鎸侀渶璋冩暣锛夛紝鎺ㄨ崘 {summary.recommended.customerName}锛堟湀渚?{recommended.monthlyPayment/100} 鍏冿級銆嶃€?- 濡傛灉 `availableCount == 0`锛屾寜"棣栦粯/鏈熸暟"寮傚父鏇村鐨勪竴绫荤粰鍑鸿皟鏁村缓璁€?- `filtered` 鍒嗙粍锛坈alculate=null 涓?termSupported=true 鐨勬棤鏄庢樉鍘熷洜澶辫触椤癸級**涓嶄富鍔ㄦ姤缁欑敤鎴?*銆?
## 閿欒澶勭悊

| 鎯呭喌 | 澶勭悊 |
|---|---|
| `cli.py match` 杩斿洖 `status=none` | 鍛婄煡鐢ㄦ埛骞跺垪鍑?`availableModelNames` |
| `cli.py match` 杩斿洖 `status=multiple` | 灞曠ず `candidates[].modelName` 璁╃敤鎴风簿纭寚瀹?|
| `cli.py terms` / `car-models` / `aggregate` 閫€鍑虹爜 != 0 | 鍘熸牱杞堪 stderr 閿欒骞剁粓姝紱**涓嶅緱浣跨敤浠讳綍鏈湴鍏滃簳鏁版嵁缁х画** |
| 鐢ㄦ埛鏃㈡病缁欓噾棰濅篃娌＄粰姣斾緥 | 璇㈤棶銆岃闂寜棣栦粯閲戦杩樻槸棣栦粯姣斾緥璇曠畻锛熴€?|
| 鐢ㄦ埛涓や釜閮界粰浜?| 鍛婄煡鍙兘浜岄€変竴锛涙渶缁堜互閲戦褰㈡€佽皟鐢?`cli.py calc-down` |
| `aggregate.hasFinancialScheme == false` | 鍛婄煡璇ヨ溅鍨嬪綋鍓嶆棤鍙敤閲戣瀺鏂规 |
| `cli.py evaluate` 澶辫触 | 杞堪 stderr 閿欒锛涗笉瑕佽倝鐪间唬鏇垮畠瑙ｆ瀽 schemes |

## Safety Rules

- **涓嶈浼€?`carModelId`**锛氬繀椤绘潵鑷?`cli.py match` 鎴?`cli.py car-models` 鍝嶅簲銆?- **涓嶈鍦ㄤ富浼氳瘽鍋氫换浣曟暟瀛﹁繍绠?*锛氫竴鍒囬噾棰?姣斾緥/鏈堜緵/棣栦粯鍖洪棿璁＄畻浜ょ粰 CLI銆傚嵆渚夸綘"涓€鐪煎氨鑳界湅鍑? 5 涓?脳 30% = 1.5 涓囷紝涔熻璧?CLI锛岄伩鍏嶅崟浣嶆悶閿欍€?- **涓嶈鍦ㄤ富浼氳瘽鐩存帴璋?HTTP 鎺ュ彛**锛氫竴鍒?`GET` / `POST` 閫氳繃 `cli.py` 鐨勫瓙鍛戒护銆?- **涓嶈鍑蹇嗗啓鏈熸暟鍒楄〃**锛氭瘡娆￠渶瑕佸€欓€夋湡鏁伴兘杩愯 `cli.py terms`銆?- **涓嶈浣跨敤鍏滃簳鏁版嵁**锛欳LI 澶辫触涓€寰嬪師鏍锋姤閿欑粓姝㈡祦绋嬶紝绂佹鎶?榛樿 [12,24,36,48,60]"涔嬬被鐨勫厹搴曚紶缁欎笅娓搞€?- **鎹㈢畻閫忔槑鎬?*锛氭瘮渚?鈫?閲戦鐨勬崲绠楃粨鏋滆鏄庣ず缁欑敤鎴凤紙濡?鎸?30% 脳 21.99 涓囷紝CLI 璁＄畻棣栦粯 65,970 鍏?锛夛紝閬垮厤鐢ㄦ埛浠ヤ负鎺ュ彛鐩存帴娑堣垂浜嗘瘮渚嬨€?- **涓ョ鍦ㄧ敤鎴峰伐浣滅洰褰曪紙CWD锛夋垨椤圭洰鐩綍钀藉湴浠讳綍鏂囦欢**銆侰LI 鍐呴儴鍙鍐呭瓨鍜屾爣鍑嗚緭鍏ヨ緭鍑猴紝涓嶅啓涓存椂鏂囦欢锛涗富浼氳瘽涔熶笉瑕佸啓 `payload.json` 涔嬬被鐨勬枃浠躲€?- **灞曠ず鍓嶉噾棰濆崟浣嶆崲绠?*锛欳LI 杩斿洖鐨勬墍鏈夐噾棰濋兘鏄?*鍒?*锛屽睍绀虹粰鐢ㄦ埛鍓嶄竴寰嬮櫎浠?100 杞厓锛屽繀瑕佹椂鍐嶉櫎浠?10000 杞竾鍏冿紱**灞曠ず鏃跺繀椤讳繚鐣欎袱浣嶅皬鏁版垨鎸夊父璇嗗彇鏁?*锛屼笉瑕佸睍绀鸿８鍒嗐€?- **绂佹灞曠ず涔辩爜瀛楁**锛欳LI 宸插己鍒?UTF-8 I/O锛涘鏋滀綘鐪嬪埌 `customerName` / `description` 浠嶆槸涔辩爜锛岃鏄庣粓绔覆鏌撻棶棰橈紙Windows cp936 绛夛級锛?*涓嶈鎶婁贡鐮佸綋鐪熷睍绀虹粰鐢ㄦ埛**锛屼篃涓嶈"鎺ㄦ祴缈昏瘧"锛屽簲鍒囨崲涓?瀛楄妭娴佺閬?+ 鏄惧紡 UTF-8 瑙ｇ爜"鏂瑰紡閲嶈窇锛堣 Step D 绀轰緥锛夈€?
## 鎵╁睍锛氱洿鎺ユ妸 core 浣滀负搴撲娇鐢紙鍙€夛級

`scripts/core/*` 鍏ㄦ槸绾嚱鏁帮紝澶辫触鎶?`MiCarTrialError`銆傚鏋滀綘鎯冲啓鑴氭湰鑰屼笉鏄皟 CLI锛屼篃鍙互锛?
```python
import sys, os
sys.path.insert(0, "<skill-base>/scripts")
from core.car_models import match_car_model
from core.aggregate import post_aggregate
from core.evaluate import evaluate_schemes

car = match_car_model("SU7 Pro")["car"]
agg = post_aggregate(int(car["carModelId"]), int(car["totalAmount"]), 5000000, 36)
result = evaluate_schemes(agg, 5000000, 36, int(car["totalAmount"]))
```

> 浣嗗湪 skill 杩愯鏃讹紙涓讳細璇濋噷锛夛紝**浠嶇劧鍙厑璁歌蛋 CLI**鈥斺€攃ore 涓嶅仛 stdout/閫€鍑虹爜绾﹀畾锛屼細璁?skill 鐨?鑴氭湰澶辫触灏卞師鏍锋姤閿?鍚堢害闅句互淇濊瘉銆?