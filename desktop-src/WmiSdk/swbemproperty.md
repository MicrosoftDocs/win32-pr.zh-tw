---
description: Swbempropertyset 物件代表 managed 物件的單一 WMI 屬性。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: 'Swbempropertyset 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195226"
---
# <a name="swbemproperty-object"></a>Swbempropertyset 物件

**Swbempropertyset** 物件代表 managed 物件的單一 WMI 屬性。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**Swbempropertyset** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Swbempropertyset** 物件具有這些屬性。



| 屬性                                                     | 存取類型           | Description                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | 唯讀<br/>  | 這個屬性的型別。<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | 唯讀<br/>  | 指出此屬性是否有陣列類型的布林值。<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | 唯讀<br/>  | 指出此屬性是否為本機的布林值。<br/>                                                            |
| [**Name**](swbemproperty-name.md)<br/>                | 唯讀<br/>  | 此 WMI 屬性的名稱。<br/>                                                                                         |
| [**起源**](swbemproperty-origin.md)<br/>            | 唯讀<br/>  | 包含這個屬性的原始類別。<br/>                                                                   |
| [**限定詞\_**](swbemproperty-qualifiers-.md)<br/> | 唯讀<br/>  | [**SWbemQualifierSet**](swbemqualifierset.md)物件，這個物件是這個屬性的限定詞集合。<br/> |
| [**值**](swbemproperty-value.md)<br/>              | 讀取/寫入<br/> | 這個屬性的實際值。 這是此物件的預設 automation 屬性。<br/>                             |



 

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




