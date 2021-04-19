---
title: LISTBOX. fontFace
description: FontFace 屬性會指定或抓取清單方塊控制項的字型。
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990203"
---
# <a name="listboxfontface"></a><span data-ttu-id="bd810-104">LISTBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="bd810-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="bd810-105">**FontFace** 屬性會指定或抓取清單方塊控制項的字型。</span><span class="sxs-lookup"><span data-stu-id="bd810-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="bd810-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="bd810-106">Possible Values</span></span>

<span data-ttu-id="bd810-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="bd810-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd810-108">備註</span><span class="sxs-lookup"><span data-stu-id="bd810-108">Remarks</span></span>

<span data-ttu-id="bd810-109">這個屬性可以是 Windows 中可用之任何有效字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd810-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="bd810-110">Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。</span><span class="sxs-lookup"><span data-stu-id="bd810-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="bd810-111">如果指定的 **fontFace** 無法在使用者的系統上使用，則清單方塊控制項預設為 Windows 系統字型。</span><span class="sxs-lookup"><span data-stu-id="bd810-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="bd810-112">英文系統的預設值是「Tahoma」。</span><span class="sxs-lookup"><span data-stu-id="bd810-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="bd810-113">針對國際系統，預設會從資源檔載入。</span><span class="sxs-lookup"><span data-stu-id="bd810-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd810-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd810-114">Requirements</span></span>



| <span data-ttu-id="bd810-115">需求</span><span class="sxs-lookup"><span data-stu-id="bd810-115">Requirement</span></span> | <span data-ttu-id="bd810-116">值</span><span class="sxs-lookup"><span data-stu-id="bd810-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="bd810-117">版本</span><span class="sxs-lookup"><span data-stu-id="bd810-117">Version</span></span><br/> | <span data-ttu-id="bd810-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bd810-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd810-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd810-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd810-120">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="bd810-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="bd810-121">**LISTBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="bd810-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="bd810-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="bd810-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





