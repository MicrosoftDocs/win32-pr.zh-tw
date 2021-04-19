---
title: 'IDWriteFontSetBuilder AddFontFaceReference 方法 (Dwrite \_ 3 .h) '
description: 將字型的參考加入至所建立的集合。
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- AddFontFaceReference 方法直接寫入
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993427"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>IDWriteFontSetBuilder：： AddFontFaceReference 方法

將字型的參考加入至所建立的集合。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference (IDWriteFontFaceReference \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | 將字型的參考加入至所建立的集合。 在呼叫 CreateFontSet 時，將會自動從字型中解壓縮必要的中繼資料。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference (IDWriteFontFaceReference \* ，CONST DWRITE \_ FONT \_ 屬性 \* ，UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | 將字型的參考加入至所建立的集合。 呼叫端會提供足夠的資訊來進行搜尋，以避免需要開啟可能的非本機字型。 不會遺漏任何由呼叫端提供的屬性，而且這些屬性將無法在 GetMatchingFonts 中做為篩選準則使用。 遺漏屬性的 System.configuration.settingsprovider.getpropertyvalues 會傳回空的字串清單。 傳遞的屬性通常應該與實際的字型內容一致，但是它們不需要。 例如，您可以使用不同的名稱或唯一識別碼來別名字型，也可以設定不存在於實際字型的自訂標記。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dwrite \_ 3。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
