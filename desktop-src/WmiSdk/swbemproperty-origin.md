---
description: Swbempropertyset 物件的 [原始] 屬性會抓取引入這個屬性之 WMI 類別的名稱。 針對具有深度繼承階層的類別，通常需要知道哪些屬性已在哪些類別中宣告。
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: 'Swbempropertyset：屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193061"
---
# <a name="swbempropertyorigin-property"></a>Swbempropertyset 屬性

[**Swbempropertyset**](swbemproperty.md)物件的 [**原始**] 屬性會抓取引入這個屬性之 WMI 類別的名稱。 針對具有深度繼承階層的類別，通常需要知道哪些屬性已在哪些類別中宣告。

如果屬性為 local (請參閱 [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)) ，此值與擁有類別相同。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbempropertyset<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




