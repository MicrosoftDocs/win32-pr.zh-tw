---
description: 將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: 'ID3DX10Font：:P reloadCharacters 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992534"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="0517d-103">ID3DX10Font：:P reloadCharacters 方法</span><span class="sxs-lookup"><span data-stu-id="0517d-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="0517d-104">將一連串字元載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="0517d-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0517d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0517d-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="0517d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0517d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0517d-107">*First* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0517d-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0517d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0517d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0517d-109">要載入視訊記憶體之第一個字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0517d-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="0517d-110">*Last* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0517d-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0517d-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0517d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0517d-112">要載入視訊記憶體之最後一個字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0517d-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0517d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0517d-113">Return value</span></span>

<span data-ttu-id="0517d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0517d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0517d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0517d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0517d-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="0517d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0517d-117">備註</span><span class="sxs-lookup"><span data-stu-id="0517d-117">Remarks</span></span>

<span data-ttu-id="0517d-118">這個方法會產生包含代表輸入字元之字元的材質。</span><span class="sxs-lookup"><span data-stu-id="0517d-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="0517d-119">圖像會繪製成一系列的三角形。</span><span class="sxs-lookup"><span data-stu-id="0517d-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="0517d-120">字元將不會轉譯至裝置;ID3DX10Font：仍然必須呼叫:D rawText 來轉譯字元。</span><span class="sxs-lookup"><span data-stu-id="0517d-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="0517d-121">不過，藉由將字元預先載入視訊記憶體，ID3DX10Font：:D rawText 將會使用明顯較少的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="0517d-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="0517d-122">這個方法會在內部使用 GDI 函數 [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85))將字元轉換成字元。</span><span class="sxs-lookup"><span data-stu-id="0517d-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="0517d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0517d-123">Requirements</span></span>



| <span data-ttu-id="0517d-124">需求</span><span class="sxs-lookup"><span data-stu-id="0517d-124">Requirement</span></span> | <span data-ttu-id="0517d-125">值</span><span class="sxs-lookup"><span data-stu-id="0517d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0517d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0517d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0517d-127"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="0517d-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0517d-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="0517d-128">Library</span></span><br/> | <dl> <span data-ttu-id="0517d-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0517d-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0517d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0517d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0517d-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="0517d-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="0517d-132">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="0517d-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
