---
title: IDWriteTextFormat1 介面
description: 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 |IDWriteTextFormat1 介面
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- IDWriteTextFormat1 介面直接寫入
- IDWriteTextFormat1 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979861"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="dfe3e-106">IDWriteTextFormat1 介面</span><span class="sxs-lookup"><span data-stu-id="dfe3e-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="dfe3e-107">描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="dfe3e-108">這個介面具有與 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 相同的所有方法，並新增了套用明確方向的能力。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="dfe3e-109">成員</span><span class="sxs-lookup"><span data-stu-id="dfe3e-109">Members</span></span>

<span data-ttu-id="dfe3e-110">**IDWriteTextFormat1** 介面繼承自 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="dfe3e-111">**IDWriteTextFormat1** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dfe3e-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="dfe3e-112">方法</span><span class="sxs-lookup"><span data-stu-id="dfe3e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dfe3e-113">方法</span><span class="sxs-lookup"><span data-stu-id="dfe3e-113">Methods</span></span>

<span data-ttu-id="dfe3e-114">**IDWriteTextFormat1** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="dfe3e-115">方法</span><span class="sxs-lookup"><span data-stu-id="dfe3e-115">Method</span></span>                                                                                | <span data-ttu-id="dfe3e-116">描述</span><span class="sxs-lookup"><span data-stu-id="dfe3e-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfe3e-117">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="dfe3e-118">取得目前的回退。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-118">Gets the current fallback.</span></span> <span data-ttu-id="dfe3e-119">如果建立配置之後未曾設定任何內容，則會是 nullptr。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="dfe3e-120">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="dfe3e-121">取得最後一行的包裝模式。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="dfe3e-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="dfe3e-123">取得文字格式的光學邊界對齊。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="dfe3e-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="dfe3e-125">使用垂直閱讀方向時，取得字型的慣用方向。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="dfe3e-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="dfe3e-127">將自訂字型回套用至版面配置。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="dfe3e-128">如果未設定任何值，則會使用預設的系統 fallback 清單。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="dfe3e-129">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="dfe3e-130">設定最後一行的包裝模式。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="dfe3e-131">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="dfe3e-132">設定文字格式的光學邊界對齊。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="dfe3e-133">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="dfe3e-134">設定文字格式的方向。</span><span class="sxs-lookup"><span data-stu-id="dfe3e-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="dfe3e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfe3e-135">Requirements</span></span>



| <span data-ttu-id="dfe3e-136">需求</span><span class="sxs-lookup"><span data-stu-id="dfe3e-136">Requirement</span></span> | <span data-ttu-id="dfe3e-137">值</span><span class="sxs-lookup"><span data-stu-id="dfe3e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe3e-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfe3e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe3e-139">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfe3e-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="dfe3e-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfe3e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe3e-141">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfe3e-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="dfe3e-142">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="dfe3e-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="dfe3e-143">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfe3e-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="dfe3e-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="dfe3e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfe3e-145"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfe3e-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dfe3e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="dfe3e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfe3e-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfe3e-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dfe3e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfe3e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe3e-149">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="dfe3e-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

