---
description: 建立字型物件。請注意，我們建議您不要使用這個函式，而是使用 DirectWrite 和 DirectXTK library SpriteFont 類別。
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: 'D3DX10CreateFontIndirect 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322771"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="31237-103">D3DX10CreateFontIndirect 函式</span><span class="sxs-lookup"><span data-stu-id="31237-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="31237-104">建立字型物件。</span><span class="sxs-lookup"><span data-stu-id="31237-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="31237-105">我們建議您不要使用這個函式，而是使用 [DirectWrite](../directwrite/direct-write-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteFont** 類別。</span><span class="sxs-lookup"><span data-stu-id="31237-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="31237-106">語法</span><span class="sxs-lookup"><span data-stu-id="31237-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="31237-107">參數</span><span class="sxs-lookup"><span data-stu-id="31237-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31237-108">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31237-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31237-109">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="31237-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="31237-110">[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="31237-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="31237-111">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31237-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31237-112">類型： **Const [**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="31237-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="31237-113">[**D3DX10 \_ 字型 \_ DESC**](d3dx10-font-desc.md)結構的指標，描述要建立之字型物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="31237-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="31237-114">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontIndirectW。</span><span class="sxs-lookup"><span data-stu-id="31237-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="31237-115">否則，函式呼叫會解析為 D3DXCreateFontIndirectA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="31237-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="31237-116">*ppFont* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="31237-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31237-117">類型： **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="31237-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="31237-118">傳回 [**ID3DX10Font 介面**](id3dx10font.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="31237-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31237-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="31237-119">Return value</span></span>

<span data-ttu-id="31237-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31237-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31237-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="31237-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31237-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="31237-122">Requirements</span></span>



| <span data-ttu-id="31237-123">需求</span><span class="sxs-lookup"><span data-stu-id="31237-123">Requirement</span></span> | <span data-ttu-id="31237-124">值</span><span class="sxs-lookup"><span data-stu-id="31237-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31237-125">標頭</span><span class="sxs-lookup"><span data-stu-id="31237-125">Header</span></span><br/>  | <dl> <span data-ttu-id="31237-126"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="31237-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="31237-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="31237-127">Library</span></span><br/> | <dl> <span data-ttu-id="31237-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="31237-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31237-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31237-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31237-130">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="31237-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
