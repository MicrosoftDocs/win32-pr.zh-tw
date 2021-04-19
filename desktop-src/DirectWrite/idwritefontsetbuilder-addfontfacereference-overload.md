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
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="95ee7-104">IDWriteFontSetBuilder：： AddFontFaceReference 方法</span><span class="sxs-lookup"><span data-stu-id="95ee7-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="95ee7-105">將字型的參考加入至所建立的集合。</span><span class="sxs-lookup"><span data-stu-id="95ee7-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="95ee7-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="95ee7-106">Overload list</span></span>



| <span data-ttu-id="95ee7-107">方法</span><span class="sxs-lookup"><span data-stu-id="95ee7-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="95ee7-108">描述</span><span class="sxs-lookup"><span data-stu-id="95ee7-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ee7-109">[**AddFontFaceReference (IDWriteFontFaceReference \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="95ee7-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="95ee7-110">將字型的參考加入至所建立的集合。</span><span class="sxs-lookup"><span data-stu-id="95ee7-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="95ee7-111">在呼叫 CreateFontSet 時，將會自動從字型中解壓縮必要的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="95ee7-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="95ee7-112">[**AddFontFaceReference (IDWriteFontFaceReference \* ，CONST DWRITE \_ FONT \_ 屬性 \* ，UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="95ee7-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="95ee7-113">將字型的參考加入至所建立的集合。</span><span class="sxs-lookup"><span data-stu-id="95ee7-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="95ee7-114">呼叫端會提供足夠的資訊來進行搜尋，以避免需要開啟可能的非本機字型。</span><span class="sxs-lookup"><span data-stu-id="95ee7-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="95ee7-115">不會遺漏任何由呼叫端提供的屬性，而且這些屬性將無法在 GetMatchingFonts 中做為篩選準則使用。</span><span class="sxs-lookup"><span data-stu-id="95ee7-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="95ee7-116">遺漏屬性的 System.configuration.settingsprovider.getpropertyvalues 會傳回空的字串清單。</span><span class="sxs-lookup"><span data-stu-id="95ee7-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="95ee7-117">傳遞的屬性通常應該與實際的字型內容一致，但是它們不需要。</span><span class="sxs-lookup"><span data-stu-id="95ee7-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="95ee7-118">例如，您可以使用不同的名稱或唯一識別碼來別名字型，也可以設定不存在於實際字型的自訂標記。</span><span class="sxs-lookup"><span data-stu-id="95ee7-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95ee7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="95ee7-119">Requirements</span></span>



| <span data-ttu-id="95ee7-120">需求</span><span class="sxs-lookup"><span data-stu-id="95ee7-120">Requirement</span></span> | <span data-ttu-id="95ee7-121">值</span><span class="sxs-lookup"><span data-stu-id="95ee7-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95ee7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="95ee7-122">Header</span></span><br/> | <dl> <span data-ttu-id="95ee7-123"><dt>Dwrite \_ 3。h</dt></span><span class="sxs-lookup"><span data-stu-id="95ee7-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ee7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95ee7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ee7-125">**IDWriteFontSetBuilder**</span><span class="sxs-lookup"><span data-stu-id="95ee7-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="95ee7-126">�</span><span class="sxs-lookup"><span data-stu-id="95ee7-126">�</span></span>

<span data-ttu-id="95ee7-127">�</span><span class="sxs-lookup"><span data-stu-id="95ee7-127">�</span></span>
