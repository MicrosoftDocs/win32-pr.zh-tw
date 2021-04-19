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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222856"
---
# <a name="xmint2-structure"></a><span data-ttu-id="05a01-104">XMINT2 結構</span><span class="sxs-lookup"><span data-stu-id="05a01-104">XMINT2 structure</span></span>

<span data-ttu-id="05a01-105">描述2D 整數向量。</span><span class="sxs-lookup"><span data-stu-id="05a01-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a01-106">語法</span><span class="sxs-lookup"><span data-stu-id="05a01-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="05a01-107">成員</span><span class="sxs-lookup"><span data-stu-id="05a01-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="05a01-108">**x**</span><span class="sxs-lookup"><span data-stu-id="05a01-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="05a01-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="05a01-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="05a01-110">**y**</span><span class="sxs-lookup"><span data-stu-id="05a01-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="05a01-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="05a01-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="05a01-112">備註</span><span class="sxs-lookup"><span data-stu-id="05a01-112">Remarks</span></span>

<span data-ttu-id="05a01-113">此結構定義于 ``D3DX\_DXGIFormatConvert.inl`` DIRECTX SDK 的標頭中， (2010 年6月) ，以從 c + + 使用。</span><span class="sxs-lookup"><span data-stu-id="05a01-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="05a01-114">在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中，此標頭的最新版本不會再定義它，而會改為依賴 DirectXMath 中的 [DIRECTX：： XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) 。</span><span class="sxs-lookup"><span data-stu-id="05a01-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="05a01-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a01-115">Requirements</span></span>



| <span data-ttu-id="05a01-116">需求</span><span class="sxs-lookup"><span data-stu-id="05a01-116">Requirement</span></span> | <span data-ttu-id="05a01-117">值</span><span class="sxs-lookup"><span data-stu-id="05a01-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a01-118">標頭</span><span class="sxs-lookup"><span data-stu-id="05a01-118">Header</span></span><br/> | <dl> <span data-ttu-id="05a01-119"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="05a01-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a01-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a01-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a01-121">結構</span><span class="sxs-lookup"><span data-stu-id="05a01-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="05a01-122">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="05a01-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
