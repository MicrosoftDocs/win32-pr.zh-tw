---
description: 您可以使用 SWbemQualifier 物件的屬性來代表 WMI 類別、實例、屬性或方法參數的單一限定詞。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: 'SWbemQualifier 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192056"
---
# <a name="swbemqualifier-object"></a>SWbemQualifier 物件

您可以使用 **SWbemQualifier** 物件的屬性來代表 WMI 類別、實例、屬性或方法參數的單一限定詞。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemQualifier** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SWbemQualifier** 物件具有這些屬性。



| 屬性                                                                       | 存取類型           | Description                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**IsAmended**](swbemqualifier-isamended.md)<br/>                       | 唯讀<br/>  | 布林值，指出是否已使用合併作業來當地語系化此限定詞。<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | 唯讀<br/>  | 指出此限定詞是否為本機的布林值。<br/>                                   |
| [**IsOverridable**](swbemqualifier-isoverridable.md)<br/>               | 讀取/寫入<br/> | 指出是否可以在傳播時覆寫此限定詞的布林值。<br/>          |
| [**Name**](swbemqualifier-name.md)<br/>                                 | 唯讀<br/>  | 此辨識符號的名稱。<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | 讀取/寫入<br/> | 布林值，指出此限定詞是否可以傳播至實例。<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | 唯讀<br/>  | 指出是否可以將此限定詞傳播至子類別的布林值。<br/>            |
| [**值**](swbemqualifier-value.md)<br/>                               | 讀取/寫入<br/> | 此辨識符號的變異值。 這是此物件的預設屬性。<br/>              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifier<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemQualifier<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




