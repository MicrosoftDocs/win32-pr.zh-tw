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
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000402"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="8646a-104">IDWriteFontSet：： System.configuration.settingsprovider.getpropertyvalues 方法</span><span class="sxs-lookup"><span data-stu-id="8646a-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="8646a-105">傳回字型集合的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8646a-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8646a-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="8646a-106">Overload list</span></span>



| <span data-ttu-id="8646a-107">方法</span><span class="sxs-lookup"><span data-stu-id="8646a-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="8646a-108">描述</span><span class="sxs-lookup"><span data-stu-id="8646a-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8646a-109">[**System.configuration.settingsprovider.getpropertyvalues (DWRITE \_ 字型 \_ 屬性 \_ 識別碼、IDWriteStringList \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="8646a-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="8646a-110">傳回集合中所有唯一的屬性值，此值可用於顯示系列清單或標記雲端等用途。</span><span class="sxs-lookup"><span data-stu-id="8646a-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="8646a-111">無論語言為何，都會傳回所有值，包括所有當地語系化的名稱。</span><span class="sxs-lookup"><span data-stu-id="8646a-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="8646a-112">[**System.configuration.settingsprovider.getpropertyvalues (DWRITE \_ FONT \_ PROPERTY \_ ID、const WCHAR \* 、IDWriteStringList \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="8646a-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="8646a-113">傳回集合中所有唯一的屬性值，此值可用於顯示系列清單或標記雲端等用途。</span><span class="sxs-lookup"><span data-stu-id="8646a-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="8646a-114">系統會根據語言清單以優先權順序傳回值，因此，如果字型包含一個以上的當地語系化名稱，則會傳回慣用的名稱。</span><span class="sxs-lookup"><span data-stu-id="8646a-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="8646a-115">[**System.configuration.settingsprovider.getpropertyvalues (UINT32，DWRITE \_ FONT \_ PROPERTY \_ ID，BOOL \* ，IDWriteLocalizedStrings \* \*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="8646a-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="8646a-116">傳回特定字型專案索引的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8646a-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="8646a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8646a-117">Requirements</span></span>



| <span data-ttu-id="8646a-118">需求</span><span class="sxs-lookup"><span data-stu-id="8646a-118">Requirement</span></span> | <span data-ttu-id="8646a-119">值</span><span class="sxs-lookup"><span data-stu-id="8646a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8646a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8646a-120">Header</span></span><br/> | <dl> <span data-ttu-id="8646a-121"><dt>Dwrite \_ 3。h</dt></span><span class="sxs-lookup"><span data-stu-id="8646a-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8646a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8646a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8646a-123">**IDWriteFontSet**</span><span class="sxs-lookup"><span data-stu-id="8646a-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="8646a-124">�</span><span class="sxs-lookup"><span data-stu-id="8646a-124">�</span></span>

<span data-ttu-id="8646a-125">�</span><span class="sxs-lookup"><span data-stu-id="8646a-125">�</span></span>
