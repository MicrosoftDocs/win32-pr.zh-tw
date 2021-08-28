---
description: 以下列出用來定義 View 提供者類別的限定詞。
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: 視圖提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7890effa0e8edd07edbb9506f88a78ceffc65fcb8d19bf6c8bcf67860a677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130970"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>視圖提供者專用的限定詞

以下列出用來定義 View 提供者類別的限定詞。

> [!Note]  
> 視圖提供者類別在使用遠端參考時，僅支援 NetBIOS 名稱。 如果您在遠端參考中使用 IP 位址或 DNS 名稱，則連線會失敗並出現0x800706ba 錯誤。

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**直接**
</dt> <dd>

資料類型： **布林值**

與 view 關聯屬性一起使用，以防止關聯參考對應至 view 參考。

下列範例會將屬性 **GroupComponent** 定義為未在 view 參考中對應的關聯參考。


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

資料類型： **布林值**

根據具有不同預設值之來源類別屬性的視圖類別屬性預設值。 基礎來源類別是由視圖隱含的。

例如，來源類別 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) 具有 [布林值](boolean.md) 屬性 **RunRepeatedly** ，指出是否要定期或只執行一次作業。 **Win32 \_ register-scheduledjob** 的預設值 **RunRepeatedly** 不是 true，但 view 類別的預設值為 true。


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**
</dt> <dd>

資料類型： **字串**

定義在聯結視圖類別中聯結來源類別實例的方式。 下列範例顯示如何使用 **JoinOn** 限定詞來聯結兩個來源類別。


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**
</dt> <dd>

資料類型： **字串陣列**

要針對 view 方法執行的來源方法。 如需類似的語法，請參閱 [PropertySources 限定詞](propertysources-qualifier.md)。 方法的簽章必須完全符合來源類別的簽章。 從定義來源類別的 MOF 檔案複製方法簽章。 下列範例會從 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))的 [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile)方法定義方法：


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



只有在搭配聯集視圖使用時，此限定詞才有效。

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

資料類型： **字串**

WQL 查詢在聯結類別聯結之後篩選實例。

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

資料類型： **字串陣列**

View 類別屬性從中取得資料的來源屬性。

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**聯盟**
</dt> <dd>

資料類型： **布林值**

指出您是否要定義聯集類別。 聯集視圖包含以來源實例聯集為基礎的實例。 例如，您可以宣告下列各項：


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

資料類型： **字串陣列**

WMI 查詢語言 (WQL) 查詢的集合，可定義特定視圖類別中所使用的來源實例和屬性。 所有陣列限定詞的位置對應都很重要。

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

資料類型： **字串陣列**

來源實例所在的命名空間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

