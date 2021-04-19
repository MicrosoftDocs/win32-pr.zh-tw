---
title: XMUINT4 結構
description: 描述4D 不帶正負號的整數向量。
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 結構 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222846"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="41f97-104">XMUINT4 結構</span><span class="sxs-lookup"><span data-stu-id="41f97-104">XMUINT4 structure</span></span>

<span data-ttu-id="41f97-105">描述4D 不帶正負號的整數向量。</span><span class="sxs-lookup"><span data-stu-id="41f97-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f97-106">語法</span><span class="sxs-lookup"><span data-stu-id="41f97-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="41f97-107">成員</span><span class="sxs-lookup"><span data-stu-id="41f97-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41f97-108">**x**</span><span class="sxs-lookup"><span data-stu-id="41f97-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="41f97-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="41f97-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="41f97-110">**y**</span><span class="sxs-lookup"><span data-stu-id="41f97-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="41f97-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="41f97-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="41f97-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="41f97-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="41f97-113">向量的 z 元件。</span><span class="sxs-lookup"><span data-stu-id="41f97-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="41f97-114">**w**</span><span class="sxs-lookup"><span data-stu-id="41f97-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="41f97-115">w-向量的元件。</span><span class="sxs-lookup"><span data-stu-id="41f97-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="41f97-116">備註</span><span class="sxs-lookup"><span data-stu-id="41f97-116">Remarks</span></span>

<span data-ttu-id="41f97-117">此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。</span><span class="sxs-lookup"><span data-stu-id="41f97-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="41f97-118">在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) 。</span><span class="sxs-lookup"><span data-stu-id="41f97-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="41f97-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="41f97-119">Requirements</span></span>



| <span data-ttu-id="41f97-120">需求</span><span class="sxs-lookup"><span data-stu-id="41f97-120">Requirement</span></span> | <span data-ttu-id="41f97-121">值</span><span class="sxs-lookup"><span data-stu-id="41f97-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f97-122">標頭</span><span class="sxs-lookup"><span data-stu-id="41f97-122">Header</span></span><br/> | <dl> <span data-ttu-id="41f97-123"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="41f97-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f97-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41f97-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f97-125">結構</span><span class="sxs-lookup"><span data-stu-id="41f97-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="41f97-126">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="41f97-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
