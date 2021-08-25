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
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898068"
---
# <a name="swbemproperty-object"></a>Swbempropertyset 物件

**Swbempropertyset** 物件代表 managed 物件的單一 WMI 屬性。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**Swbempropertyset** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Swbempropertyset** 物件具有這些屬性。



| 屬性                                                     | 存取類型           | 描述                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | 唯讀<br/>  | 這個屬性的型別。<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | 唯讀<br/>  | 指出此屬性是否有陣列類型的布林值。<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | 唯讀<br/>  | 指出此屬性是否為本機的布林值。<br/>                                                            |
| [**名稱**](swbemproperty-name.md)<br/>                | 唯讀<br/>  | 此 WMI 屬性的名稱。<br/>                                                                                         |
| [**起源**](swbemproperty-origin.md)<br/>            | 唯讀<br/>  | 包含這個屬性的原始類別。<br/>                                                                   |
| [**限定詞\_**](swbemproperty-qualifiers-.md)<br/> | 唯讀<br/>  | [**SWbemQualifierSet**](swbemqualifierset.md)物件，這個物件是這個屬性的限定詞集合。<br/> |
| [**值**](swbemproperty-value.md)<br/>              | 讀取/寫入<br/> | 這個屬性的實際值。 這是此物件的預設 automation 屬性。<br/>                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbempropertyset<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




