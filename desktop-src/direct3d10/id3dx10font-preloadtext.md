---
description: 將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。 這個方法支援 ANSI 和 Unicode 字串。
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: 'ID3DX10Font：:P reloadText 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196277"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="8b4f4-104">ID3DX10Font：:P reloadText 方法</span><span class="sxs-lookup"><span data-stu-id="8b4f4-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="8b4f4-105">將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="8b4f4-106">這個方法支援 ANSI 和 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b4f4-107">語法</span><span class="sxs-lookup"><span data-stu-id="8b4f4-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="8b4f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b4f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b4f4-109">*pString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b4f4-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b4f4-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b4f4-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b4f4-111">要載入視訊記憶體的字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="8b4f4-112">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR;否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="8b4f4-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8b4f4-114">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b4f4-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b4f4-115">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b4f4-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b4f4-116">文字字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b4f4-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b4f4-117">Return value</span></span>

<span data-ttu-id="8b4f4-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b4f4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b4f4-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8b4f4-120">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b4f4-121">備註</span><span class="sxs-lookup"><span data-stu-id="8b4f4-121">Remarks</span></span>

<span data-ttu-id="8b4f4-122">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8b4f4-123">如果已定義 Unicode，函式呼叫會解析為 PreloadTextW。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="8b4f4-124">否則，函式呼叫會解析為 PreloadTextA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="8b4f4-125">這個方法會產生包含代表輸入文字之字元的材質。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="8b4f4-126">圖像會繪製成一系列的三角形。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="8b4f4-127">系統不會將文字轉譯至裝置;ID3DX10Font：仍然必須呼叫:D rawText，才能呈現文字。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="8b4f4-128">不過，藉由將文字預先載入視訊記憶體，ID3DX10Font：:D rawText 將會使用明顯較少的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="8b4f4-129">這個方法會在內部使用 GDI 函數 [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85))將字元轉換成字元。</span><span class="sxs-lookup"><span data-stu-id="8b4f4-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4f4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b4f4-130">Requirements</span></span>



| <span data-ttu-id="8b4f4-131">需求</span><span class="sxs-lookup"><span data-stu-id="8b4f4-131">Requirement</span></span> | <span data-ttu-id="8b4f4-132">值</span><span class="sxs-lookup"><span data-stu-id="8b4f4-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4f4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8b4f4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8b4f4-134"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4f4-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b4f4-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b4f4-135">Library</span></span><br/> | <dl> <span data-ttu-id="8b4f4-136"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b4f4-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4f4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b4f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4f4-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="8b4f4-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="8b4f4-139">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8b4f4-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
