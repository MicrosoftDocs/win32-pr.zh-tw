---
title: FontFace
description: FontFace 屬性會指定或抓取文字控制項的字樣。
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- FontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994349"
---
# <a name="textfontface"></a><span data-ttu-id="89301-104">FontFace</span><span class="sxs-lookup"><span data-stu-id="89301-104">TEXT.fontFace</span></span>

<span data-ttu-id="89301-105">**FontFace** 屬性會指定或抓取文字控制項的字樣。</span><span class="sxs-lookup"><span data-stu-id="89301-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="89301-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="89301-106">Possible Values</span></span>

<span data-ttu-id="89301-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="89301-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89301-108">備註</span><span class="sxs-lookup"><span data-stu-id="89301-108">Remarks</span></span>

<span data-ttu-id="89301-109">這個屬性可以是 Windows 上任何可用的有效字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="89301-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="89301-110">Windows Media Player 將不支援安裝字型，因此請選擇您知道將會在預期系統上的字型。</span><span class="sxs-lookup"><span data-stu-id="89301-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="89301-111">如果使用者的系統無法使用指定的 **fontFace** ，文字控制項會預設為 Windows 系統字型。</span><span class="sxs-lookup"><span data-stu-id="89301-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="89301-112">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="89301-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="89301-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="89301-113">Requirements</span></span>



| <span data-ttu-id="89301-114">需求</span><span class="sxs-lookup"><span data-stu-id="89301-114">Requirement</span></span> | <span data-ttu-id="89301-115">值</span><span class="sxs-lookup"><span data-stu-id="89301-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="89301-116">版本</span><span class="sxs-lookup"><span data-stu-id="89301-116">Version</span></span><br/> | <span data-ttu-id="89301-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="89301-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89301-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89301-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89301-119">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="89301-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="89301-120">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="89301-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





