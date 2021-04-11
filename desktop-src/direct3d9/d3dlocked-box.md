---
description: 描述 (磁片區) 的鎖定箱。
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: 'D3DLOCKED_BOX 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196312"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="1802c-103">D3DLOCKED \_ BOX 結構</span><span class="sxs-lookup"><span data-stu-id="1802c-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="1802c-104">描述 (磁片區) 的鎖定箱。</span><span class="sxs-lookup"><span data-stu-id="1802c-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="1802c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1802c-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="1802c-106">成員</span><span class="sxs-lookup"><span data-stu-id="1802c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1802c-107">**RowPitch**</span><span class="sxs-lookup"><span data-stu-id="1802c-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="1802c-108">類型： **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1802c-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1802c-109">從某個資料列的左邊緣到下一個資料列的左邊緣的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="1802c-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="1802c-110">**SlicePitch**</span><span class="sxs-lookup"><span data-stu-id="1802c-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="1802c-111">類型： **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1802c-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1802c-112">從一個配量左上角到下一個最深配量左上角的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="1802c-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="1802c-113">**pBits**</span><span class="sxs-lookup"><span data-stu-id="1802c-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="1802c-114">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="1802c-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="1802c-115">磁片區方塊開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="1802c-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="1802c-116">如果將 [**D3DBOX**](d3dbox.md) 提供給加密箱呼叫，pBits 將會從磁片區的開頭適當地位移。</span><span class="sxs-lookup"><span data-stu-id="1802c-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1802c-117">備註</span><span class="sxs-lookup"><span data-stu-id="1802c-117">Remarks</span></span>

<span data-ttu-id="1802c-118">您可以將磁片區視覺化成寬度 x 高度2D 表面的配量，以形成寬度 x 高度 x 深度音量。</span><span class="sxs-lookup"><span data-stu-id="1802c-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="1802c-119">如需詳細資訊，請參閱 [ (Direct3D 9) 的音量材質資源 ](volume-texture-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="1802c-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1802c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1802c-120">Requirements</span></span>



| <span data-ttu-id="1802c-121">需求</span><span class="sxs-lookup"><span data-stu-id="1802c-121">Requirement</span></span> | <span data-ttu-id="1802c-122">值</span><span class="sxs-lookup"><span data-stu-id="1802c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1802c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1802c-123">Header</span></span><br/> | <dl> <span data-ttu-id="1802c-124"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1802c-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1802c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1802c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1802c-126">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="1802c-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="1802c-127">**IDirect3DVolume9：：加密箱**</span><span class="sxs-lookup"><span data-stu-id="1802c-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="1802c-128">**IDirect3DVolumeTexture9：：加密箱**</span><span class="sxs-lookup"><span data-stu-id="1802c-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
