---
description: SWbemRefresher 物件的 AutoReconnect 屬性是一個布林值，指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: 'SWbemRefresher. AutoReconnect 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312810"
---
# <a name="swbemrefresherautoreconnect-property"></a>SWbemRefresher. AutoReconnect 屬性

[**SWbemRefresher**](swbemrefresher.md)物件的 **AutoReconnect** 屬性是一個布林值，指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

修改此屬性只會影響重新整理程式中由高效能提供者所支援的物件。 如果提供者不是高效能的提供者，則將 **AutoReconnect** 屬性設定為 **TRUE** 不會有任何作用，因為 [**SWbemRefresher**](swbemrefresher.md) 物件永遠不會重新連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




