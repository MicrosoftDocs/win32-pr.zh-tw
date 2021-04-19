---
title: 編輯方塊. fontFace
description: FontFace 屬性會指定或抓取編輯方塊控制項中文字的字型。
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- 編輯方塊. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984390"
---
# <a name="editboxfontface"></a><span data-ttu-id="c1f12-104">編輯方塊. fontFace</span><span class="sxs-lookup"><span data-stu-id="c1f12-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="c1f12-105">**FontFace** 屬性會指定或抓取編輯方塊控制項中文字的字型。</span><span class="sxs-lookup"><span data-stu-id="c1f12-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="c1f12-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c1f12-106">Possible Values</span></span>

<span data-ttu-id="c1f12-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="c1f12-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f12-108">備註</span><span class="sxs-lookup"><span data-stu-id="c1f12-108">Remarks</span></span>

<span data-ttu-id="c1f12-109">這個屬性可以是 Windows 中可用之任何有效字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1f12-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="c1f12-110">Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。</span><span class="sxs-lookup"><span data-stu-id="c1f12-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="c1f12-111">如果使用者的系統無法使用指定的 **fontFace** ，編輯方塊控制項就會預設為 Windows 系統字型。</span><span class="sxs-lookup"><span data-stu-id="c1f12-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="c1f12-112">英文系統的預設值是「Tahoma」。</span><span class="sxs-lookup"><span data-stu-id="c1f12-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="c1f12-113">針對國際系統，預設會從資源檔載入。</span><span class="sxs-lookup"><span data-stu-id="c1f12-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f12-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1f12-114">Requirements</span></span>



| <span data-ttu-id="c1f12-115">需求</span><span class="sxs-lookup"><span data-stu-id="c1f12-115">Requirement</span></span> | <span data-ttu-id="c1f12-116">值</span><span class="sxs-lookup"><span data-stu-id="c1f12-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="c1f12-117">版本</span><span class="sxs-lookup"><span data-stu-id="c1f12-117">Version</span></span><br/> | <span data-ttu-id="c1f12-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c1f12-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1f12-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1f12-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f12-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="c1f12-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="c1f12-121">**編輯方塊. fontSize**</span><span class="sxs-lookup"><span data-stu-id="c1f12-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="c1f12-122">**編輯方塊. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="c1f12-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





