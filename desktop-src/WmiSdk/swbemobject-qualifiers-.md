---
description: '\_SWbemObject 物件的限定詞屬性會傳回 SWbemQualifierSet 物件，該物件為目前類別或實例的限定詞集合。 這是唯讀的屬性。'
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: 'SWbemObject.Qualifiers_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732488"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject 的限定詞 \_ 屬性

[**SWbemObject**](swbemobject.md)物件的 **限定詞 \_** 屬性會傳回 [**SWbemQualifierSet**](swbemqualifierset.md)物件，該物件為目前類別或實例的限定詞集合。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

TechNet 元件庫上 WMI 類別 VBScript 程式碼範例的 [所有限定詞都](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) 是使用 [辨識符號] \_ 屬性來列出所指定 WMI 類別的類別限定詞。

TechNet 元件庫上 WMI VBScript 程式碼範例 [中的所有抽象類別清單](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) 會列出根 \\ cimv2 命名空間中定義的所有 wmi 抽象類別。

列出 WMI VBScript 程式碼範例 [中的所有動態類別](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) 會使用限定詞 \_ 屬性來列出所有 WMI 動態類別 (包括根 \\ cimv2 命名空間中定義的關聯類別) 。

TechNet 元件庫上的 [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell 程式碼範例會列出指定之命名空間中的所有可寫入屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




