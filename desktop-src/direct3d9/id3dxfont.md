---
description: ID3DXFont 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: 'ID3DXFont 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000628"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="7f292-103">ID3DXFont 介面</span><span class="sxs-lookup"><span data-stu-id="7f292-103">ID3DXFont interface</span></span>

<span data-ttu-id="7f292-104">ID3DXFont 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。</span><span class="sxs-lookup"><span data-stu-id="7f292-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="7f292-105">成員</span><span class="sxs-lookup"><span data-stu-id="7f292-105">Members</span></span>

<span data-ttu-id="7f292-106">**ID3DXFont** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7f292-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7f292-107">**ID3DXFont** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f292-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="7f292-108">方法</span><span class="sxs-lookup"><span data-stu-id="7f292-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f292-109">方法</span><span class="sxs-lookup"><span data-stu-id="7f292-109">Methods</span></span>

<span data-ttu-id="7f292-110">**ID3DXFont** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f292-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="7f292-111">方法</span><span class="sxs-lookup"><span data-stu-id="7f292-111">Method</span></span>                                                    | <span data-ttu-id="7f292-112">描述</span><span class="sxs-lookup"><span data-stu-id="7f292-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f292-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="7f292-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="7f292-114">繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="7f292-114">Draws formatted text.</span></span> <span data-ttu-id="7f292-115">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="7f292-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="7f292-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="7f292-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="7f292-117">傳回已設定字型 (DC) 的顯示裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="7f292-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="7f292-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7f292-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="7f292-119">取得目前字型物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7f292-119">Gets a description of the current font object.</span></span> <span data-ttu-id="7f292-120">GetDescW 和 GetDescA 與這個方法相同，不同之處在于指標會分別傳回至 [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) 或 **D3DXFONT \_ DESCA** 結構。</span><span class="sxs-lookup"><span data-stu-id="7f292-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="7f292-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="7f292-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="7f292-122">抓取與字型物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="7f292-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="7f292-123">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="7f292-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="7f292-124">傳回字元資料格中圖像位置和方向的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f292-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="7f292-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="7f292-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="7f292-126">捕獲 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中所識別的字型特性。</span><span class="sxs-lookup"><span data-stu-id="7f292-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="7f292-127">這個方法支援 ANSI 和 Unicode 編譯器設定。</span><span class="sxs-lookup"><span data-stu-id="7f292-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="7f292-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="7f292-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="7f292-129">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="7f292-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="7f292-130">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f292-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="7f292-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="7f292-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="7f292-132">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="7f292-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="7f292-133">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="7f292-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="7f292-134">將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="7f292-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="7f292-135">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="7f292-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="7f292-136">將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="7f292-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="7f292-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="7f292-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="7f292-138">將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="7f292-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="7f292-139">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="7f292-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="7f292-140">備註</span><span class="sxs-lookup"><span data-stu-id="7f292-140">Remarks</span></span>

<span data-ttu-id="7f292-141">**ID3DXFont** 介面的取得方式是呼叫 [**D3DXCreateFont**](d3dxcreatefont.md)或 [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md)。</span><span class="sxs-lookup"><span data-stu-id="7f292-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="7f292-142">LPD3DXFONT 型別定義為 **ID3DXFont** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7f292-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="7f292-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f292-143">Requirements</span></span>



| <span data-ttu-id="7f292-144">需求</span><span class="sxs-lookup"><span data-stu-id="7f292-144">Requirement</span></span> | <span data-ttu-id="7f292-145">值</span><span class="sxs-lookup"><span data-stu-id="7f292-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f292-146">標頭</span><span class="sxs-lookup"><span data-stu-id="7f292-146">Header</span></span><br/>  | <dl> <span data-ttu-id="7f292-147"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f292-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7f292-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f292-148">Library</span></span><br/> | <dl> <span data-ttu-id="7f292-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f292-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f292-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f292-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f292-151">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="7f292-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
