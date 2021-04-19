---
title: IDWriteFactory2 介面
description: 所有 DirectWrite 物件的根 factory 介面。
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- IDWriteFactory1 介面直接寫入
- IDWriteFactory1 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999609"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="97087-105">IDWriteFactory2 介面</span><span class="sxs-lookup"><span data-stu-id="97087-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="97087-106">所有 [DirectWrite](direct-write-portal.md) 物件的根 factory 介面。</span><span class="sxs-lookup"><span data-stu-id="97087-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="97087-107">成員</span><span class="sxs-lookup"><span data-stu-id="97087-107">Members</span></span>

<span data-ttu-id="97087-108">**IDWriteFactory1** 介面繼承自 [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)。</span><span class="sxs-lookup"><span data-stu-id="97087-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="97087-109">**IDWriteFactory2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97087-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="97087-110">方法</span><span class="sxs-lookup"><span data-stu-id="97087-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97087-111">方法</span><span class="sxs-lookup"><span data-stu-id="97087-111">Methods</span></span>

<span data-ttu-id="97087-112">**IDWriteFactory1** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="97087-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="97087-113">方法</span><span class="sxs-lookup"><span data-stu-id="97087-113">Method</span></span>                                                                             | <span data-ttu-id="97087-114">描述</span><span class="sxs-lookup"><span data-stu-id="97087-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97087-115">**CreateCustomRenderingParams**</span><span class="sxs-lookup"><span data-stu-id="97087-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="97087-116">使用指定的屬性建立呈現參數物件。</span><span class="sxs-lookup"><span data-stu-id="97087-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="97087-117">**CreateFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="97087-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="97087-118">建立字型 fallback builder 物件。</span><span class="sxs-lookup"><span data-stu-id="97087-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="97087-119">**CreateGlyphRunAnalysis**</span><span class="sxs-lookup"><span data-stu-id="97087-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="97087-120">建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="97087-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="97087-121">**GetSystemFontFallback**</span><span class="sxs-lookup"><span data-stu-id="97087-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="97087-122">從系統字型 fallback 清單建立字型回溯物件。</span><span class="sxs-lookup"><span data-stu-id="97087-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="97087-123">**TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="97087-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="97087-124">在圖像執行上呼叫這個方法，以將它轉譯成多個色彩字元執行。</span><span class="sxs-lookup"><span data-stu-id="97087-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="97087-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="97087-125">Requirements</span></span>



| <span data-ttu-id="97087-126">需求</span><span class="sxs-lookup"><span data-stu-id="97087-126">Requirement</span></span> | <span data-ttu-id="97087-127">值</span><span class="sxs-lookup"><span data-stu-id="97087-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97087-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97087-128">Minimum supported client</span></span><br/> | <span data-ttu-id="97087-129">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97087-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="97087-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97087-130">Minimum supported server</span></span><br/> | <span data-ttu-id="97087-131">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97087-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="97087-132">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="97087-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="97087-133">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97087-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="97087-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="97087-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="97087-135"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97087-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="97087-136">DLL</span><span class="sxs-lookup"><span data-stu-id="97087-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97087-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97087-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97087-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97087-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97087-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="97087-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="97087-140">**IDWriteFactory**</span><span class="sxs-lookup"><span data-stu-id="97087-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

