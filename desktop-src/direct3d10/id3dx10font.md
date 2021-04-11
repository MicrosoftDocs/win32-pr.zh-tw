---
description: ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: 'ID3DX10Font 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196278"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="a9f38-103">ID3DX10Font 介面</span><span class="sxs-lookup"><span data-stu-id="a9f38-103">ID3DX10Font interface</span></span>

<span data-ttu-id="a9f38-104">ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。</span><span class="sxs-lookup"><span data-stu-id="a9f38-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="a9f38-105">成員</span><span class="sxs-lookup"><span data-stu-id="a9f38-105">Members</span></span>

<span data-ttu-id="a9f38-106">**ID3DX10Font** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a9f38-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9f38-107">**ID3DX10Font** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9f38-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="a9f38-108">方法</span><span class="sxs-lookup"><span data-stu-id="a9f38-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9f38-109">方法</span><span class="sxs-lookup"><span data-stu-id="a9f38-109">Methods</span></span>

<span data-ttu-id="a9f38-110">**ID3DX10Font** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a9f38-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="a9f38-111">方法</span><span class="sxs-lookup"><span data-stu-id="a9f38-111">Method</span></span>                                                     | <span data-ttu-id="a9f38-112">描述</span><span class="sxs-lookup"><span data-stu-id="a9f38-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9f38-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="a9f38-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="a9f38-114">繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="a9f38-114">Draw formatted text.</span></span> <span data-ttu-id="a9f38-115">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="a9f38-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="a9f38-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="a9f38-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="a9f38-117">傳回已將字型設定在其上的顯示裝置內容 (DC) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a9f38-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="a9f38-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a9f38-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="a9f38-119">取得目前字型物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a9f38-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a9f38-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="a9f38-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="a9f38-121">取出與字型物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="a9f38-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="a9f38-122">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="a9f38-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="a9f38-123">傳回字元資料格中圖像位置和方向的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9f38-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="a9f38-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="a9f38-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="a9f38-125">取得字型特性。</span><span class="sxs-lookup"><span data-stu-id="a9f38-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="a9f38-126">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="a9f38-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="a9f38-127">將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="a9f38-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="a9f38-128">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="a9f38-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="a9f38-129">將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="a9f38-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="a9f38-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="a9f38-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="a9f38-131">將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="a9f38-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="a9f38-132">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="a9f38-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9f38-133">備註</span><span class="sxs-lookup"><span data-stu-id="a9f38-133">Remarks</span></span>

<span data-ttu-id="a9f38-134">ID3DX10Font 介面的取得方式是呼叫 [**D3DX10CreateFont**](d3dx10createfont.md) 或 [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f38-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="a9f38-135">LPD3DX10FONT 型別定義為 ID3DX10Font 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a9f38-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="a9f38-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f38-136">Requirements</span></span>



| <span data-ttu-id="a9f38-137">需求</span><span class="sxs-lookup"><span data-stu-id="a9f38-137">Requirement</span></span> | <span data-ttu-id="a9f38-138">值</span><span class="sxs-lookup"><span data-stu-id="a9f38-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f38-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a9f38-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a9f38-140"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f38-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9f38-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9f38-141">Library</span></span><br/> | <dl> <span data-ttu-id="a9f38-142"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9f38-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f38-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9f38-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f38-144">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a9f38-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
