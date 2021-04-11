---
description: WMI 命令列 (WMIC) 公用程式提供適用于 WMI 的命令列介面。
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed46e8aeab24acb44f51099a6e813e921dd77eaa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196149"
---
# <a name="wmic"></a>wmic

WMI 命令列 (WMIC) 公用程式提供命令列介面，Windows Management Instrumentation (WMI) 。 WMIC 與現有的 shell 和公用程式命令相容。 以下是適用于 WMIC 的一般參考主題。 如需有關如何使用 WMIC 的詳細資訊和指導方針，包括別名、動詞、交換器和命令的其他資訊，請參閱 [使用 Windows Management Instrumentation 命令列](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) 和 [WMIC-透過 WMI 進行命令列控制](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10))。

## <a name="alias"></a>Alias

別名是類別、屬性或方法的易記重新命名，可讓 WMI 更容易使用和讀取。 您可以透過/，判斷哪些別名可用於 WMIC **？** 。 您也可以使用 **<className> /？** 來決定特定類別的別名。 。 如需詳細資訊，請參閱 [WMIC 別名](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10))。

## <a name="switch"></a>參數

交換器是您可以全域設定或選擇性設定的 WMIC 選項。 如需可用參數的清單，請參閱 [WMIC 參數](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10))。

## <a name="verbs"></a>動詞

若要在 WMIC 中使用動詞，請輸入別名名稱，後面接著動詞。 如果別名不支援動詞，您會收到訊息「提供者不能進行嘗試的作業。」 如需詳細資訊，請參閱 [WMIC 動詞](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10))。

大部分的別名都支援下列動詞。

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>ASSOC
</dt> <dd>

`Associators of (<wmi_object>)`傳回查詢的結果，其中 *<wmi \_ 物件>* 是 **path** 或 **CLASS** 命令所傳回之物件的路徑。 結果是與物件相關聯的實例。 當 ASSOC 搭配別名使用時，會傳回具有該別名之類別的類別。 依預設，輸出會以 HTML 格式傳回。

ASSOC 動詞有下列參數。



| Switch                         | 描述                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | 與來源物件相關聯的傳回端點必須屬於或衍生自指定的類別。      |
| /RESULTROLE:<rolename>   | 傳回的端點必須在與來源物件的關聯中播放特定的角色。                              |
| /ASSOCCLASS:<assocclass> | 傳回的端點必須透過指定的類別或其中一個衍生類別，與來源建立關聯。 |



 

範例： **作業系統 ASSOC**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>叫
</dt> <dd>

執行方法。

範例： **服務的標題 = ' TELNET ' 呼叫 STARTSERVICE**

> [!Note]  
> 若要判斷指定類別的可用方法，請使用 **/？**。 例如， **服務的標題 = ' TELNET ' CALL/？** 列出服務類別的可用功能。

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>創建
</dt> <dd>

建立新的實例，並設定屬性值。 CREATE 不能用來建立新的類別。

範例： **環境 CREATE NAME = "TEMP";VARIABLEVALUE = "NEW"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>刪除
</dt> <dd>

刪除目前的實例或實例的集合。 DELETE 可以用來刪除類別。

範例： **NAME = "CALC.EXE" DELETE 的進程**

</dd> <dt>

<span id="GET"></span><span id="get"></span>獲取
</dt> <dd>

取出特定屬性值。

GET 具有下列參數。



| Switch                               | 描述                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | 輸出會以個別行上所列出的每個值和屬性的名稱來格式化。                                           |
| /ALL                                 | 輸出會格式化為表格。                                                                                                            |
| 來源語言<translation table> | 使用命令所命名的轉譯資料表來轉譯輸出。 BasicXml 和 NoComma 的轉譯資料表會隨附于 WMIC。 |
| 台<interval>              | 每秒重複命令 <interval> 。                                                                                         |
| 形式<format specifier>     | 指定要格式化資料的關鍵單字或 XSL 檔案名。                                                                                  |



 

範例： **進程 GET 名稱**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>清單
</dt> <dd>

顯示資料。 LIST 是預設動詞。

清單具有下列副詞。



| 副詞   | Description                                                  |
|----------|--------------------------------------------------------------|
| 簡短    | 屬性的核心集。                                  |
| FULL     | 完整的屬性集。 這是清單的預設副詞。 |
| INSTANCE | 僅限實例路徑。                                         |
| 狀態   | 物件的狀態。                                       |
| 系統   | 系統屬性。                                           |



 

清單具有下列參數。



| Switch                               | 描述                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 來源語言<translation table> | 使用命令所命名的轉譯資料表來轉譯輸出。 BasicXml 和 NoComma 的轉譯資料表會隨附于 WMIC。 |
| 台<interval>              | 每秒重複命令 <interval> 。                                                                                         |
| 形式<format specifier>     | 指定要格式化資料的關鍵單字或 XSL 檔案名。                                                                                  |



 

範例： **流程清單簡介**

</dd> <dt>

<span id="SET"></span><span id="set"></span>設置
</dt> <dd>

將值指派給屬性。 範例： **環境集合名稱 = "TEMP"**， **VARIABLEVALUE = "NEW"**

</dd> </dl>

## <a name="switches"></a>交換器

全域參數是用來設定 WMIC 環境的預設值。 您可以藉由輸入 **內容** 命令來查看這些參數所設定之條件的目前值。

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

別名通常使用的命名空間。 預設值為根 \\ cimv2。

範例： **/NAMESPACE： \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

命名空間 WMIC 通常會尋找別名和其他 WMIC 資訊。

範例： **/ROLE： \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

電腦名稱稱（以逗號分隔）。 所有命令都會針對此值中列出的所有電腦進行同步執行。 檔案名前面必須加上 &。 檔案內的電腦名稱稱必須以逗號分隔，或在個別的行上。

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

模擬等級。

範例： **/IMPLEVEL： Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

驗證層級。

範例： **/AUTHLEVEL： Pkt**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

現場。

範例： **/LOCALE： MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

啟用或停用擁有權限。

範例： **/PRIVILEGES： ENABLE** 或 **/PRIVILEGES： DISABLE**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

顯示所有用來執行 WMIC 命令的函式的成功或失敗。

範例： **/TRACE： ON** 或 **/TRACE： OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

記錄 XML 檔案的所有輸出。 輸出也會顯示在命令提示字元中。

範例： **/RECORD：** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

通常會確認刪除命令。

範例： **/INTERACTIVE： ON** 或 **/INTERACTIVE： OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

如果在/NODE 電腦上，會在傳送 WMIC 命令給它們之前進行 ping。 如果電腦沒有回應，就不會將這些命令傳送給它。

範例： "/FAILFAST： ON" 或 "/FAILFAST： OFF"

**WMIC/FAILFAST：1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

當存取/NODE 電腦或別名中所指定的電腦時，由 WMIC 使用的使用者名稱。 系統會提示您輸入密碼。 使用者名稱不能與本機電腦搭配使用。

範例： **/user：**_JSMITH_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

WMIC 在存取/NPDE 電腦時所使用的密碼。 在命令列可以看到密碼。

範例： **/password：**_PASSWORD_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

指定所有輸出重新導向的模式。 輸出不會出現在命令列中，而且會在開始輸出之前清除目的地。 有效的值為 STDOUT、剪貼簿或檔案名。

範例： **/OUTPUT：剪貼** 簿

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

指定所有輸出重新導向的模式。 輸出不會出現在命令列中，而且不會在開始輸出之前清除目的地，並且會將輸出附加至目的地目前內容的結尾。 有效的值為 STDOUT、剪貼簿或檔案名。

範例： **/APPEND：剪貼** 簿

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

搭配 **LIST** 和 **GET/EVERY** 參數使用。 如果匯總為 ON，當/NODE 中的所有電腦都已回應或超時時，LIST 和 GET 會顯示其結果。如果匯總為 OFF，則會在收到結果時立即列出並顯示其結果。

範例： **/AGGREGATE： OFF** 或 **/AGGREGATE： ON**

</dd> </dl>

## <a name="commands"></a>命令

下列 WMIC 命令隨時都可供使用。 如需詳細資訊，請參閱 [WMIC 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10))。

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>類
</dt> <dd>

從預設的 WMIC 別名模式進行 Escape，以直接存取 WMI 架構中的類別。 如需可用 WMI 類別的詳細資訊，請參閱 [Wmi 類別](wmi-classes.md)。

範例： **WMIC/OUTPUT： c： \\ClassOutput.htm 類別 Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>路徑
</dt> <dd>

從預設的 WMIC 別名模式進行 Escape，以直接存取 WMI 架構中的實例。

範例： **WMIC/OUTPUT： c： \\PathOutput.txt PATH WIN32 \_ SoundDevice GET/VALUE**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>上下文
</dt> <dd>

顯示所有全域參數的目前值。

範例： **WMIC 內容**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>退出
</dt> <dd>

退出 WMIC。

範例： **WMIC QUIT**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>退出
</dt> <dd>

退出 WMIC。

範例： **WMIC EXIT**

</dd> </dl>

## <a name="examples"></a>範例

使用 TechNet 資源庫上的 [wmic 範例設定 ip/子網/閘道/dns 的腳本](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) ，說明如何修改和更新 Ip、子網、閘道和 dns 設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

