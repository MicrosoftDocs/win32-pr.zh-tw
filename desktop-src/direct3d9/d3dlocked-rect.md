---
description: 描述鎖定的矩形區域。
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: 'D3DLOCKED_RECT 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514629"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="0fb20-103">D3DLOCKED \_ RECT 結構</span><span class="sxs-lookup"><span data-stu-id="0fb20-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="0fb20-104">描述鎖定的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="0fb20-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb20-105">語法</span><span class="sxs-lookup"><span data-stu-id="0fb20-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="0fb20-106">成員</span><span class="sxs-lookup"><span data-stu-id="0fb20-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fb20-107">**瀝青**</span><span class="sxs-lookup"><span data-stu-id="0fb20-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="0fb20-108">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0fb20-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0fb20-109">介面中一個資料列的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0fb20-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="0fb20-110">**pBits**</span><span class="sxs-lookup"><span data-stu-id="0fb20-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="0fb20-111">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="0fb20-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="0fb20-112">鎖定位的指標。</span><span class="sxs-lookup"><span data-stu-id="0fb20-112">Pointer to the locked bits.</span></span> <span data-ttu-id="0fb20-113">如果將 [**RECT**](/previous-versions//dd162897(v=vs.85)) 提供給 [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 呼叫，pBits 將會從表面的開頭開始進行適當的位移。</span><span class="sxs-lookup"><span data-stu-id="0fb20-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fb20-114">備註</span><span class="sxs-lookup"><span data-stu-id="0fb20-114">Remarks</span></span>

<span data-ttu-id="0fb20-115">DXTn 格式的音調與 DirectX 7 中所傳回的格式不同。</span><span class="sxs-lookup"><span data-stu-id="0fb20-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="0fb20-116">它現在是指區塊資料列中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0fb20-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="0fb20-117">例如，如果您的寬度是16，則會有4個區塊 (4 \* 個 DXT1，4 \* 16 DXT2-5。 ) </span><span class="sxs-lookup"><span data-stu-id="0fb20-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb20-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fb20-118">Requirements</span></span>



| <span data-ttu-id="0fb20-119">需求</span><span class="sxs-lookup"><span data-stu-id="0fb20-119">Requirement</span></span> | <span data-ttu-id="0fb20-120">值</span><span class="sxs-lookup"><span data-stu-id="0fb20-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb20-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0fb20-121">Header</span></span><br/> | <dl> <span data-ttu-id="0fb20-122"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb20-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb20-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fb20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb20-124">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="0fb20-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="0fb20-125">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="0fb20-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="0fb20-126">**IDirect3DSurface9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="0fb20-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="0fb20-127">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="0fb20-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
