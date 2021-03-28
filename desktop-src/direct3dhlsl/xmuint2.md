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
ms.openlocfilehash: 73d14bd43ec3b75a2bf503b7d742b6c69881475b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974440"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="b964e-104">XMUINT2 結構</span><span class="sxs-lookup"><span data-stu-id="b964e-104">XMUINT2 structure</span></span>

<span data-ttu-id="b964e-105">描述2D 不帶正負號的整數向量。</span><span class="sxs-lookup"><span data-stu-id="b964e-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b964e-106">語法</span><span class="sxs-lookup"><span data-stu-id="b964e-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="b964e-107">成員</span><span class="sxs-lookup"><span data-stu-id="b964e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b964e-108">**x**</span><span class="sxs-lookup"><span data-stu-id="b964e-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b964e-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="b964e-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="b964e-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b964e-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b964e-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="b964e-111">y-component of the vector.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b964e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b964e-112">Requirements</span></span>



| <span data-ttu-id="b964e-113">需求</span><span class="sxs-lookup"><span data-stu-id="b964e-113">Requirement</span></span> | <span data-ttu-id="b964e-114">值</span><span class="sxs-lookup"><span data-stu-id="b964e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b964e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b964e-115">Header</span></span><br/> | <dl> <span data-ttu-id="b964e-116"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="b964e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b964e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b964e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b964e-118">結構</span><span class="sxs-lookup"><span data-stu-id="b964e-118">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="b964e-119">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="b964e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





