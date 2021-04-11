---
description: 將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont：:P reloadGlyphs 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035428"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="aaa2d-103">ID3DXFont：:P reloadGlyphs 方法</span><span class="sxs-lookup"><span data-stu-id="aaa2d-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="aaa2d-104">將一連串的字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="aaa2d-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="aaa2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaa2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa2d-107">*First* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa2d-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa2d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaa2d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aaa2d-109">要載入視訊記憶體的第一個圖像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="aaa2d-110">*Last* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaa2d-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa2d-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aaa2d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aaa2d-112">要載入視訊記憶體之最後一個圖像的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa2d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaa2d-113">Return value</span></span>

<span data-ttu-id="aaa2d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aaa2d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aaa2d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="aaa2d-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa2d-117">備註</span><span class="sxs-lookup"><span data-stu-id="aaa2d-117">Remarks</span></span>

<span data-ttu-id="aaa2d-118">這個方法會產生包含輸入字型的材質。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="aaa2d-119">圖像會繪製成一系列的三角形。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="aaa2d-120">字元不會轉譯至裝置;您仍然必須呼叫 [**DrawText**](id3dxfont--drawtext.md) 來呈現字元。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="aaa2d-121">不過，藉由將字元預先載入視訊記憶體， **DrawText** 將使用明顯較少的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="aaa2d-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa2d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaa2d-122">Requirements</span></span>



| <span data-ttu-id="aaa2d-123">需求</span><span class="sxs-lookup"><span data-stu-id="aaa2d-123">Requirement</span></span> | <span data-ttu-id="aaa2d-124">值</span><span class="sxs-lookup"><span data-stu-id="aaa2d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa2d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="aaa2d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="aaa2d-126"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa2d-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="aaa2d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="aaa2d-127">Library</span></span><br/> | <dl> <span data-ttu-id="aaa2d-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaa2d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aaa2d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaa2d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa2d-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="aaa2d-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
