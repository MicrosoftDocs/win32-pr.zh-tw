---
description: 將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: 'ID3DX10Font：:P reloadGlyphs 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000598"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="26553-103">ID3DX10Font：:P reloadGlyphs 方法</span><span class="sxs-lookup"><span data-stu-id="26553-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="26553-104">將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="26553-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="26553-105">語法</span><span class="sxs-lookup"><span data-stu-id="26553-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="26553-106">參數</span><span class="sxs-lookup"><span data-stu-id="26553-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26553-107">*First* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26553-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26553-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26553-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26553-109">要載入視訊記憶體的第一個圖像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="26553-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="26553-110">*Last* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26553-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26553-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26553-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26553-112">要載入視訊記憶體之最後一個圖像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="26553-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26553-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="26553-113">Return value</span></span>

<span data-ttu-id="26553-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26553-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26553-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="26553-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26553-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="26553-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="26553-117">備註</span><span class="sxs-lookup"><span data-stu-id="26553-117">Remarks</span></span>

<span data-ttu-id="26553-118">這個方法會產生包含輸入字型的材質。</span><span class="sxs-lookup"><span data-stu-id="26553-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="26553-119">圖像會繪製成一系列的三角形。</span><span class="sxs-lookup"><span data-stu-id="26553-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="26553-120">字元不會轉譯至裝置;ID3DX10Font：仍然必須呼叫:D rawText 來轉譯圖像。</span><span class="sxs-lookup"><span data-stu-id="26553-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="26553-121">不過，藉由將字元預先載入視訊記憶體，ID3DX10Font：:D rawText 將會使用明顯較少的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="26553-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="26553-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="26553-122">Requirements</span></span>



| <span data-ttu-id="26553-123">需求</span><span class="sxs-lookup"><span data-stu-id="26553-123">Requirement</span></span> | <span data-ttu-id="26553-124">值</span><span class="sxs-lookup"><span data-stu-id="26553-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26553-125">標頭</span><span class="sxs-lookup"><span data-stu-id="26553-125">Header</span></span><br/>  | <dl> <span data-ttu-id="26553-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="26553-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="26553-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="26553-127">Library</span></span><br/> | <dl> <span data-ttu-id="26553-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26553-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26553-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26553-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26553-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="26553-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="26553-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="26553-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
