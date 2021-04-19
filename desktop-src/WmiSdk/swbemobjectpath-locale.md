---
description: SWbemObjectPath 物件的 Locale 屬性包含物件路徑的地區設定。
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: 'SWbemObjectPath： Locale 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990328"
---
# <a name="swbemobjectpathlocale-property"></a>SWbemObjectPath。 Locale 屬性

[**SWbemObjectPath**](swbemobjectpath.md)物件的 **locale** 屬性包含物件路徑的地區設定。

當 **SWbemObjectPath. Locale** 屬性是獨立 [**SWbemObjectPath**](swbemobjectpath.md) 物件的一部分時，就會讀取/寫入，而且可以用來設定該標記的地區設定元件。

當 **SWbemObjectPath. Locale** 屬性當做 [**\_ SWbemObject. Path**](swbemobject-path-.md)屬性的一部分來存取時，它會是唯讀的，而且會報告用來系結至從中取得物件之命名空間的地區設定值。

若為 Microsoft 地區設定識別碼，則字串的格式為 "MS \_ xxxx"，其中 xxxx 是十六進位格式的字串，表示 LCID。 例如，美式英文地區設定識別碼是「MS \_ 409」。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Locale As String
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
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




