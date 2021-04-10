---
description: SWbemObjectPath 物件的索引鍵屬性是 SWbemNamedValueSet 物件，其中包含索引鍵值系結。 這是唯讀的屬性。
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: 'SWbemObjectPath，索引鍵屬性 (Adoctint) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026489"
---
# <a name="swbemobjectpathkeys-property"></a>SWbemObjectPath 索引鍵屬性

[**SWbemObjectPath**](swbemobjectpath.md)物件的索引 **鍵** 屬性是 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含索引鍵值系結。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

在您取得索引 **鍵** 屬性之後， **Err** 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100C) 
</dt> <dd>

功能或作業不支援。 如果腳本嘗試寫入這個屬性，就會傳回此錯誤。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                             |
| 標頭<br/>                   | <dl> <dt>Adoctint (包含 >wbemdisp.tlb) </dt> </dl> |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                                          |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                                           |



 

 




