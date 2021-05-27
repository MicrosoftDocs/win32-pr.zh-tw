---
title: XMUINT2 結構
description: 描述2D 不帶正負號的整數向量。
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2 結構 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549563"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="1e608-104">XMUINT2 結構</span><span class="sxs-lookup"><span data-stu-id="1e608-104">XMUINT2 structure</span></span>

<span data-ttu-id="1e608-105">描述2D 不帶正負號的整數向量。</span><span class="sxs-lookup"><span data-stu-id="1e608-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e608-106">語法</span><span class="sxs-lookup"><span data-stu-id="1e608-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="1e608-107">成員</span><span class="sxs-lookup"><span data-stu-id="1e608-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e608-108">**x**</span><span class="sxs-lookup"><span data-stu-id="1e608-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="1e608-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="1e608-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="1e608-110">**y**</span><span class="sxs-lookup"><span data-stu-id="1e608-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="1e608-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="1e608-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="1e608-112">備註</span><span class="sxs-lookup"><span data-stu-id="1e608-112">Remarks</span></span>

<span data-ttu-id="1e608-113">此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。</span><span class="sxs-lookup"><span data-stu-id="1e608-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="1e608-114">在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) 。</span><span class="sxs-lookup"><span data-stu-id="1e608-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="1e608-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e608-115">Requirements</span></span>



| <span data-ttu-id="1e608-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e608-116">Requirement</span></span> | <span data-ttu-id="1e608-117">值</span><span class="sxs-lookup"><span data-stu-id="1e608-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e608-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1e608-118">Header</span></span><br/> | <dl> <span data-ttu-id="1e608-119"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="1e608-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e608-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e608-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e608-121">結構</span><span class="sxs-lookup"><span data-stu-id="1e608-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="1e608-122">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="1e608-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>