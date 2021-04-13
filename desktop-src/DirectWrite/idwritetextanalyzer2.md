---
title: IDWriteTextAnalyzer2 介面
description: 分析不同的文字屬性以進行複雜的腳本處理。
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- IDWriteTextAnalyzer2 介面直接寫入
- IDWriteTextAnalyzer2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508795"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="b0203-105">IDWriteTextAnalyzer2 介面</span><span class="sxs-lookup"><span data-stu-id="b0203-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="b0203-106">分析不同的文字屬性以進行複雜的腳本處理。</span><span class="sxs-lookup"><span data-stu-id="b0203-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="b0203-107">成員</span><span class="sxs-lookup"><span data-stu-id="b0203-107">Members</span></span>

<span data-ttu-id="b0203-108">**IDWriteTextAnalyzer2** 介面繼承自 [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)。</span><span class="sxs-lookup"><span data-stu-id="b0203-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="b0203-109">**IDWriteTextAnalyzer2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0203-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="b0203-110">方法</span><span class="sxs-lookup"><span data-stu-id="b0203-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b0203-111">方法</span><span class="sxs-lookup"><span data-stu-id="b0203-111">Methods</span></span>

<span data-ttu-id="b0203-112">**IDWriteTextAnalyzer2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b0203-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="b0203-113">方法</span><span class="sxs-lookup"><span data-stu-id="b0203-113">Method</span></span>                                                                                    | <span data-ttu-id="b0203-114">描述</span><span class="sxs-lookup"><span data-stu-id="b0203-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0203-115">**CheckTypographicFeature**</span><span class="sxs-lookup"><span data-stu-id="b0203-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="b0203-116">檢查印刷樣式功能是否適用于圖像或一組字元。</span><span class="sxs-lookup"><span data-stu-id="b0203-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="b0203-117">**GetGlyphOrientationTransform**</span><span class="sxs-lookup"><span data-stu-id="b0203-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="b0203-118">針對各自的角度傳回2x3 轉換矩陣，以繪製圖像執行。</span><span class="sxs-lookup"><span data-stu-id="b0203-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="b0203-119">**GetTypographicFeatures**</span><span class="sxs-lookup"><span data-stu-id="b0203-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="b0203-120">傳回腳本或字型可用之 OpenType 功能的完整清單。</span><span class="sxs-lookup"><span data-stu-id="b0203-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0203-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0203-121">Requirements</span></span>



| <span data-ttu-id="b0203-122">需求</span><span class="sxs-lookup"><span data-stu-id="b0203-122">Requirement</span></span> | <span data-ttu-id="b0203-123">值</span><span class="sxs-lookup"><span data-stu-id="b0203-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0203-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0203-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0203-125">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0203-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="b0203-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0203-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0203-127">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0203-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b0203-128">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="b0203-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b0203-129">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0203-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="b0203-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="b0203-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0203-131"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0203-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b0203-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0203-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0203-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0203-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0203-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0203-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0203-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="b0203-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

