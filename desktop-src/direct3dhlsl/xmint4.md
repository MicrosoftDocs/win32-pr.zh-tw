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
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323128"
---
# <a name="xmint4-structure"></a><span data-ttu-id="9610b-104">XMINT4 結構</span><span class="sxs-lookup"><span data-stu-id="9610b-104">XMINT4 structure</span></span>

<span data-ttu-id="9610b-105">描述4D 的整數向量。</span><span class="sxs-lookup"><span data-stu-id="9610b-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9610b-106">語法</span><span class="sxs-lookup"><span data-stu-id="9610b-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="9610b-107">成員</span><span class="sxs-lookup"><span data-stu-id="9610b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9610b-108">**x**</span><span class="sxs-lookup"><span data-stu-id="9610b-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="9610b-109">向量的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="9610b-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="9610b-110">**y**</span><span class="sxs-lookup"><span data-stu-id="9610b-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="9610b-111">向量的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="9610b-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="9610b-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="9610b-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="9610b-113">向量的 z 元件。</span><span class="sxs-lookup"><span data-stu-id="9610b-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="9610b-114">**w**</span><span class="sxs-lookup"><span data-stu-id="9610b-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="9610b-115">w-向量的元件。</span><span class="sxs-lookup"><span data-stu-id="9610b-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9610b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9610b-116">Requirements</span></span>



| <span data-ttu-id="9610b-117">需求</span><span class="sxs-lookup"><span data-stu-id="9610b-117">Requirement</span></span> | <span data-ttu-id="9610b-118">值</span><span class="sxs-lookup"><span data-stu-id="9610b-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9610b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9610b-119">Header</span></span><br/> | <dl> <span data-ttu-id="9610b-120"><dt>D3DX \_ DXGIFormatConvert. .inl</dt></span><span class="sxs-lookup"><span data-stu-id="9610b-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9610b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9610b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9610b-122">結構</span><span class="sxs-lookup"><span data-stu-id="9610b-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="9610b-123">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="9610b-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





