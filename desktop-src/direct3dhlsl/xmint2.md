---
title: XMINT2 結構
description: 描述2D 整數向量。
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2 結構 HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5dfe4aab8a23dbf1b7921742272b0d2b0ab2382
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549983"
---
# <a name="xmint2-structure"></a><span data-ttu-id="bc647-104">XMINT2 結構</span><span class="sxs-lookup"><span data-stu-id="bc647-104">XMINT2 structure</span></span>

<span data-ttu-id="bc647-105">描述2D 整數向量。</span><span class="sxs-lookup"><span data-stu-id="bc647-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc647-106">語法</span><span class="sxs-lookup"><span data-stu-id="bc647-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="bc647-107">成員</span><span class="sxs-lookup"><span data-stu-id="bc647-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc647-108">**x**</span><span class="sxs-lookup"><span data-stu-id="bc647-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="bc647-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="bc647-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="bc647-110">**y**</span><span class="sxs-lookup"><span data-stu-id="bc647-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="bc647-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="bc647-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="bc647-112">備註</span><span class="sxs-lookup"><span data-stu-id="bc647-112">Remarks</span></span>

<span data-ttu-id="bc647-113">此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。</span><span class="sxs-lookup"><span data-stu-id="bc647-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="bc647-114">在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) 。</span><span class="sxs-lookup"><span data-stu-id="bc647-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="bc647-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc647-115">Requirements</span></span>



| <span data-ttu-id="bc647-116">需求</span><span class="sxs-lookup"><span data-stu-id="bc647-116">Requirement</span></span> | <span data-ttu-id="bc647-117">值</span><span class="sxs-lookup"><span data-stu-id="bc647-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc647-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bc647-118">Header</span></span><br/> | <dl> <span data-ttu-id="bc647-119"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="bc647-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc647-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc647-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc647-121">結構</span><span class="sxs-lookup"><span data-stu-id="bc647-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="bc647-122">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="bc647-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>