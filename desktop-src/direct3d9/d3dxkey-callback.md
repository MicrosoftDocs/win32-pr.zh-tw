---
description: 描述要用於主要畫面格動畫的回呼金鑰。
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: 'D3DXKEY_CALLBACK 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997388"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="bc539-103">D3DXKEY \_ 回呼結構</span><span class="sxs-lookup"><span data-stu-id="bc539-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="bc539-104">描述要用於主要畫面格動畫的回呼金鑰。</span><span class="sxs-lookup"><span data-stu-id="bc539-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc539-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc539-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="bc539-106">成員</span><span class="sxs-lookup"><span data-stu-id="bc539-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc539-107">**Time**</span><span class="sxs-lookup"><span data-stu-id="bc539-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="bc539-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc539-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bc539-109">主要畫面格時間戳記。</span><span class="sxs-lookup"><span data-stu-id="bc539-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="bc539-110">**pCallbackData**</span><span class="sxs-lookup"><span data-stu-id="bc539-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="bc539-111">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc539-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bc539-112">使用者回呼資料的指標。</span><span class="sxs-lookup"><span data-stu-id="bc539-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc539-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc539-113">Requirements</span></span>



| <span data-ttu-id="bc539-114">需求</span><span class="sxs-lookup"><span data-stu-id="bc539-114">Requirement</span></span> | <span data-ttu-id="bc539-115">值</span><span class="sxs-lookup"><span data-stu-id="bc539-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc539-116">標頭</span><span class="sxs-lookup"><span data-stu-id="bc539-116">Header</span></span><br/> | <dl> <span data-ttu-id="bc539-117"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc539-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc539-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc539-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc539-119">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="bc539-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
