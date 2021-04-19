---
title: XMINT4 結構
description: 描述4D 的整數向量。
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4 結構 HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222836"
---
# <a name="xmint4-structure"></a><span data-ttu-id="50ee3-104">XMINT4 結構</span><span class="sxs-lookup"><span data-stu-id="50ee3-104">XMINT4 structure</span></span>

<span data-ttu-id="50ee3-105">描述4D 的整數向量。</span><span class="sxs-lookup"><span data-stu-id="50ee3-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ee3-106">語法</span><span class="sxs-lookup"><span data-stu-id="50ee3-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="50ee3-107">成員</span><span class="sxs-lookup"><span data-stu-id="50ee3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="50ee3-108">**x**</span><span class="sxs-lookup"><span data-stu-id="50ee3-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="50ee3-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="50ee3-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="50ee3-110">**y**</span><span class="sxs-lookup"><span data-stu-id="50ee3-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="50ee3-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="50ee3-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="50ee3-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="50ee3-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="50ee3-113">向量的 z 元件。</span><span class="sxs-lookup"><span data-stu-id="50ee3-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="50ee3-114">**w**</span><span class="sxs-lookup"><span data-stu-id="50ee3-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="50ee3-115">w-向量的元件。</span><span class="sxs-lookup"><span data-stu-id="50ee3-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50ee3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="50ee3-116">Requirements</span></span>



| <span data-ttu-id="50ee3-117">需求</span><span class="sxs-lookup"><span data-stu-id="50ee3-117">Requirement</span></span> | <span data-ttu-id="50ee3-118">值</span><span class="sxs-lookup"><span data-stu-id="50ee3-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ee3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="50ee3-119">Header</span></span><br/> | <dl> <span data-ttu-id="50ee3-120"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="50ee3-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="50ee3-121">備註</span><span class="sxs-lookup"><span data-stu-id="50ee3-121">Remarks</span></span>

<span data-ttu-id="50ee3-122">此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。</span><span class="sxs-lookup"><span data-stu-id="50ee3-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="50ee3-123">在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) 。</span><span class="sxs-lookup"><span data-stu-id="50ee3-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="50ee3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50ee3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ee3-125">結構</span><span class="sxs-lookup"><span data-stu-id="50ee3-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="50ee3-126">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="50ee3-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
