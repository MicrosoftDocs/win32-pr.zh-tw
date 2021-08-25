---
description: 使用 Swbemobjectset 搭配使用物件的 Count 屬性，判斷 Swbemobjectset 搭配使用集合中有多少個專案。 這是唯讀的屬性。
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用： Count 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857228"
---
# <a name="swbemobjectsetcount-property"></a>Swbemobjectset 搭配使用 Count 屬性

使用 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件的 **Count** 屬性，判斷 **swbemobjectset 搭配使用** 集合中有多少個專案。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

使用 Count 時要特別注意的一點是，WMI 不會將集合中的專案數目維持在執行中的計數。 如果您要求集合的計數，WMI 無法立即以數位回應;相反地，它必須對專案進行計算，以列舉整個集合。 對於具有相當少專案的集合（例如服務），此列舉可能需要不到一秒。 不過，在事件記錄檔集合中計算事件數目可能需要更長的時間。

然後，假設您想要顯示集合中每個事件的屬性值。 若是如此，WMI 就必須第二次列舉整個集合。

> [!Note]  
> 如果您嘗試從方法傳回的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件取得這個屬性，而該方法的指定旗標包含在 wbemFlagForwardOnly 旗標中，則您會收到 wbemErrFailed 錯誤。

 

## <a name="examples"></a>範例

在大部分的情況下，您只會對 Swbemobjectset 搭配使用列舉集合本身所包含的所有物件。 不過，計數計數在系統管理腳本中很有用。 顧名思義，Count 會告訴您集合中的專案數。 例如，此腳本會取得電腦上安裝的所有服務的集合，然後回顯找到的服務總數：


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



計數會很有用，因為它可以告訴您電腦上是否有特定的實例可供使用。 例如，此腳本會在名稱為 W3SVC 的電腦上，取得所有服務的集合。 如果計數為 0 (且有效的集合沒有任何實例) ，這表示電腦上未安裝 W3SVC 服務。


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbemobjectset 搭配使用<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




