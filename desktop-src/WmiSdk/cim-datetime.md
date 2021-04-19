---
description: 您可以使用 WMI 和 CIM 專屬的兩個固定長度格式之一，來存取 WMI 中的所有通用訊息模型 (CIM) 日期和時間。 在腳本中，使用 SWbemDateTime 物件將這些轉換成一般日期和時間。
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983844"
---
# <a name="cim_datetime"></a>CIM \_ DATETIME

您可以使用 WMI 和 CIM 專屬的兩個固定長度格式之一，來存取 WMI 中的所有 [*通用訊息模型 (CIM)*](gloss-c.md) 日期和時間。 在腳本中，使用 [**SWbemDateTime**](swbemdatetime.md) 物件將這些轉換成一般日期和時間。

下列各節說明如何使用 WMI 日期和時間格式。

## <a name="format"></a>格式

下表列出 WMI 所使用的兩種日期和時間格式。



| 格式                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Datetime](datetime.md)<br/> *Yyyymmddhhmmss.ffffff. mmmmmmsUUU*<br/>                             | 儲存 CIM [**DATETIME**](datetime.md) 值的格式。 這種格式與地區設定無關，因此您可以撰寫在任何電腦上執行的腳本。 您必須使用此格式來定義 [*受控物件格式 (MOF)*](gloss-m.md)的日期和時間，或使用適用于 Wmi 的 [COM API](com-api-for-wmi.md) 或 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md)寫入至實例時的日期和時間。 如需詳細資訊，請參閱 [修改實例屬性](modifying-an-instance-property.md)。 |
| 格式只在 WMI 查詢語言 (WQL) 查詢中有效。<br/> *yyyy-mm-dd HH： MM： SS： mmm*<br/> | 此格式可用於使用 [**SWbemDateTime**](swbemdatetime.md) 方法的腳本。 如需詳細資訊，請參閱[使用 WQL](querying-with-wql.md)[查詢 WMI](querying-wmi.md)或查詢。 此格式與地區設定無關。 Year、month 和 day 的順序取決於使用者會話的地區和語言格式設定。 例如，美國英文的預設值為 "yyyy-mm-dd hh： mm： ss： mmm"，其他大部分國家或地區的格式為 "yyyy-mm-dd hh： mm： ss： mmm"。       |



 

下表列出這些格式的欄位。



| 欄位    | 描述                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *yyyy*   | 四位數年份 (0000 到 9999) 。 您的執行可以限制支援的範圍。 例如，執行只能支援年1980到2099。                                                                         |
| *mm*     | 兩位數的月份 (01 到 12) 。                                                                                                                                                                                                                |
| *dd*     | 月份的兩位數天 (01 到 31) 。 此值必須適用于月份。 例如，2月31日無效。 不過，您的執行不需要檢查是否有有效的資料。                                            |
| *HH*     | 使用24小時制的一天兩位數小時 (00 到 23) 。                                                                                                                                                                              |
| *毫米*     | 小時的兩位數分鐘 (00 到 59) 。                                                                                                                                                                                                   |
| *匯總*     | 分鐘 (00 到 59) 的兩位數秒數。                                                                                                                                                                                      |
| *mmmmmm* | 第二個數字的毫秒數， (000000 到 999999) 。 您的執行不需要使用此欄位來支援評估。 不過，這個欄位必須一律存在，以保留字元串的固定長度性質。 |
| *mmm*    | 分鐘 (000 到 999) 的三位數毫秒數。                                                                                                                                                                             |
| *s*      | 再加上正負號 (+) 或減號 (-) 表示與國際標準時間之間的正面或負面位移 (UTC) 。                                                                                                                               |
| *UUU*    | 三位數位移，表示原始時區偏離 UTC 的分鐘數。 針對 WMI，建議您但非必要，將時間轉換為 GMT (UTC 位移為零) 。                                              |



 

您必須輸入具有指定長度的所有欄位，並使用適用于該類型的前置零。 不過，請使用星號來指出未使用的欄位或萬用字元值。 \*除了查詢的 **WHERE** 子句以外，您可以在任何地方使用星號 () 。 例如，具有未指定年份的日期和時間可能會在任何年份發生。 如果您想要讓欄位保持未指定，則必須將整個欄位取代為星號。

下列範例說明有效和不正確星號用法：

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (合法) 
-   1998-04-16 \* \* \* \* \* \* ： \* \* \* (不合法的) 
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (不合法的) 
-   199 \* -04-16 \* \* \* \* \* \* ： \* \* \* (不合法的) 

如果使用 datetime 來代表特定時間點，其所有欄位都應該包含資料。 如果用來表示時間範圍，則只有傳達期間所需的欄位才會包含資料。

下列範例描述「4月前」：相對於某些未指定年份的日期，但如果測量詳細資料層級為一天，則仍是定義的點。

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* ： \* \* \* (不合法的) 

## <a name="setting-utc-offset-and-gmt"></a>設定 UTC 時差和 GMT

下列範例說明如何在加號或減號之後將星號放在 UUU 欄位中，以定義沒有時區的時間：

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000-\*\*\*
-   1998-04-01 13:58:09： \* \* \* (不合法的) 

應用程式會在執行中的作業系統內，將 unzoned 的日期和時間參考解釋為本機的抽象 chronometer。 例如，可攜式電腦可以有內部時鐘，其設定可能或不會對應至地理時區。 您可以用目前的摘要時間來源（而不是本地時區）來解讀 unzoned 時間。

您應該特別考慮 UTC 時差與查詢中日期和時間的意義。 一般情況下，當日期和時間使用相同的 UTC 位移時，等價、大於或小於比較的工作會在兩個日期和時間之間運作。 處理不同時區位移時所發生的日期和時間時，您應該先將日期和時間轉換為 GMT。

在一或多個子欄位中使用星號的相關查詢，在比較是否相等時，只對 WMI 有意義。 此外，WMI 不允許使用星號作為萬用字元。 相反地，WMI 會以字元為單位來比較相對的日期和時間。

下列範例說明 WMI 查詢不視為相等的兩個日期：

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>轉換成 FILETIME 或 VT \_ 日期格式

CIM [**DATETIME**](datetime.md) 格式只會在 WMI 內使用。 您可以藉 \_ 由呼叫 [**SWbemDateTime**](swbemdatetime.md) 腳本物件的方法，從 WMI 格式轉換為和，以及使用 FILETIME 或 VT 日期格式。 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) **datetime** 結構是32位 Windows 作業系統所使用的64位值。 VT \_ 日期格式是 Visual Basic 和 ActiveX 使用的 automation variant datetime 值。 下表列出轉換方法。



| 方法                                                         | 描述                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md) | 取得 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)格式的 [**日期時間**](datetime.md)值。                |
| [**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)   | 取得 VT 日期格式的 [**日期時間**](datetime.md) 值 \_ 。                                         |
| [**SWbemDateTime.SetFileTime**](swbemdatetime-setvardate.md)  | 使用 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)日期做為輸入，設定 [**DATETIME**](datetime.md)屬性。 |
| [**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)   | 使用 VT [](datetime.md) \_ 日期日期做為輸入，設定 DATETIME 屬性。                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[日期和時間格式](date-and-time-format.md)
</dt> <dt>

[關於 WMI](about-wmi.md)
</dt> <dt>

[WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)
</dt> <dt>

[間隔格式](interval-format.md)
</dt> <dt>

[**SWbemObject。 Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServicesEx。 Put**](swbemservicesex-put.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices：:P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

