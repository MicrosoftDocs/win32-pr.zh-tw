---
description: 針對裝置和字型間接建立字型物件。
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: 'D3DXCreateFontIndirect 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323160"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="1aaf7-103">D3DXCreateFontIndirect 函式</span><span class="sxs-lookup"><span data-stu-id="1aaf7-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="1aaf7-104">針對裝置和字型間接建立字型物件。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aaf7-105">語法</span><span class="sxs-lookup"><span data-stu-id="1aaf7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="1aaf7-106">參數</span><span class="sxs-lookup"><span data-stu-id="1aaf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aaf7-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aaf7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaf7-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1aaf7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1aaf7-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與字型物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="1aaf7-110">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aaf7-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaf7-111">Type： **Const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="1aaf7-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="1aaf7-112">[**D3DXFONT \_ DESC**](d3dxfont-desc.md)結構的指標，描述要建立之字型物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="1aaf7-113">如果編譯器設定需要 Unicode，則資料類型 D3DXFONT \_ DESC 會解析為 D3DXFONT \_ DESCW; 否則，資料類型會解析為 D3DXFONT \_ DESCA。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="1aaf7-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1aaf7-115">*ppFont* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1aaf7-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aaf7-116">類型： **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="1aaf7-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="1aaf7-117">傳回 [**ID3DXFont**](id3dxfont.md) 介面的指標，表示所建立的字型物件。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aaf7-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1aaf7-118">Return value</span></span>

<span data-ttu-id="1aaf7-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1aaf7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1aaf7-120">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1aaf7-121">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aaf7-122">備註</span><span class="sxs-lookup"><span data-stu-id="1aaf7-122">Remarks</span></span>

<span data-ttu-id="1aaf7-123">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1aaf7-124">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontIndirectW。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="1aaf7-125">否則，函式呼叫會解析為 D3DXCreateFontIndirectA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="1aaf7-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aaf7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aaf7-126">Requirements</span></span>



| <span data-ttu-id="1aaf7-127">需求</span><span class="sxs-lookup"><span data-stu-id="1aaf7-127">Requirement</span></span> | <span data-ttu-id="1aaf7-128">值</span><span class="sxs-lookup"><span data-stu-id="1aaf7-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aaf7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1aaf7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1aaf7-130"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="1aaf7-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1aaf7-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="1aaf7-131">Library</span></span><br/> | <dl> <span data-ttu-id="1aaf7-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1aaf7-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1aaf7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aaf7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aaf7-134">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="1aaf7-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
