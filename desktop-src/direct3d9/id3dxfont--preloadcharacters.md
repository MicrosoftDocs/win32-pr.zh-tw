---
description: 將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: 'ID3DXFont：:P reloadCharacters 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982238"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="be1d8-103">ID3DXFont：:P reloadCharacters 方法</span><span class="sxs-lookup"><span data-stu-id="be1d8-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="be1d8-104">將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="be1d8-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="be1d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="be1d8-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="be1d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="be1d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be1d8-107">*First* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be1d8-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be1d8-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be1d8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be1d8-109">要載入視訊記憶體之第一個字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="be1d8-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="be1d8-110">*Last* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be1d8-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be1d8-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be1d8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be1d8-112">要載入視訊記憶體之最後一個字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="be1d8-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be1d8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="be1d8-113">Return value</span></span>

<span data-ttu-id="be1d8-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be1d8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be1d8-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="be1d8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be1d8-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="be1d8-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1d8-117">備註</span><span class="sxs-lookup"><span data-stu-id="be1d8-117">Remarks</span></span>

<span data-ttu-id="be1d8-118">這個方法會產生包含代表輸入字元之字元的材質。</span><span class="sxs-lookup"><span data-stu-id="be1d8-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="be1d8-119">圖像會繪製成一系列的三角形。</span><span class="sxs-lookup"><span data-stu-id="be1d8-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="be1d8-120">字元將不會轉譯至裝置;您仍然必須呼叫 [**DrawText**](id3dxfont--drawtext.md) 來呈現字元。</span><span class="sxs-lookup"><span data-stu-id="be1d8-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="be1d8-121">不過，藉由將字元預先載入視訊記憶體， **DrawText** 將使用明顯較少的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="be1d8-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="be1d8-122">這個方法會在內部使用 GDI 函數 [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)將字元轉換成字元。</span><span class="sxs-lookup"><span data-stu-id="be1d8-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="be1d8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="be1d8-123">Requirements</span></span>



| <span data-ttu-id="be1d8-124">需求</span><span class="sxs-lookup"><span data-stu-id="be1d8-124">Requirement</span></span> | <span data-ttu-id="be1d8-125">值</span><span class="sxs-lookup"><span data-stu-id="be1d8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be1d8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="be1d8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="be1d8-127"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="be1d8-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="be1d8-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="be1d8-128">Library</span></span><br/> | <dl> <span data-ttu-id="be1d8-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be1d8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be1d8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be1d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be1d8-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="be1d8-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
