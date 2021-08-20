---
title: 'IDWriteFontSet System.configuration.settingsprovider.getpropertyvalues 方法 (Dwrite \_ 3 .h) '
description: 傳回字型集合的屬性值。
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- System.configuration.settingsprovider.getpropertyvalues 方法直接寫入
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816359"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>IDWriteFontSet：： System.configuration.settingsprovider.getpropertyvalues 方法

傳回字型集合的屬性值。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                   | 描述                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**System.configuration.settingsprovider.getpropertyvalues (DWRITE \_ 字型 \_ 屬性 \_ 識別碼、IDWriteStringList \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | 傳回集合中所有唯一的屬性值，此值可用於顯示系列清單或標記雲端等用途。 無論語言為何，都會傳回所有值，包括所有當地語系化的名稱。 <br/>                                                                                       |
| [**System.configuration.settingsprovider.getpropertyvalues (DWRITE \_ FONT \_ PROPERTY \_ ID、const WCHAR \* 、IDWriteStringList \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | 傳回集合中所有唯一的屬性值，此值可用於顯示系列清單或標記雲端等用途。 系統會根據語言清單以優先權順序傳回值，因此，如果字型包含一個以上的當地語系化名稱，則會傳回慣用的名稱。 <br/> |
| [**System.configuration.settingsprovider.getpropertyvalues (UINT32，DWRITE \_ FONT \_ PROPERTY \_ ID，BOOL \* ，IDWriteLocalizedStrings \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | 傳回特定字型專案索引的屬性值。<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dwrite \_ 3。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
