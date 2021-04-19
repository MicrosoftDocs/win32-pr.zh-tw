---
description: 識別記憶體資料。 已取代。
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: 'DXFILELOADMEMORY 結構 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999972"
---
# <a name="dxfileloadmemory-structure"></a><span data-ttu-id="225e7-104">DXFILELOADMEMORY 結構</span><span class="sxs-lookup"><span data-stu-id="225e7-104">DXFILELOADMEMORY structure</span></span>

<span data-ttu-id="225e7-105">識別記憶體資料。</span><span class="sxs-lookup"><span data-stu-id="225e7-105">Identifies memory data.</span></span> <span data-ttu-id="225e7-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="225e7-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="225e7-107">語法</span><span class="sxs-lookup"><span data-stu-id="225e7-107">Syntax</span></span>


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="225e7-108">成員</span><span class="sxs-lookup"><span data-stu-id="225e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="225e7-109">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="225e7-109">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="225e7-110">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="225e7-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="225e7-111">要載入之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="225e7-111">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="225e7-112">**dSize**</span><span class="sxs-lookup"><span data-stu-id="225e7-112">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="225e7-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="225e7-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="225e7-114">要載入之記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="225e7-114">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="225e7-115">備註</span><span class="sxs-lookup"><span data-stu-id="225e7-115">Remarks</span></span>

<span data-ttu-id="225e7-116">當應用程式使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 方法並指定 DXFILELOAD FROMMEMORY 時，此結構會識別要載入的資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="225e7-116">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="225e7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="225e7-117">Requirements</span></span>



| <span data-ttu-id="225e7-118">需求</span><span class="sxs-lookup"><span data-stu-id="225e7-118">Requirement</span></span> | <span data-ttu-id="225e7-119">值</span><span class="sxs-lookup"><span data-stu-id="225e7-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="225e7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="225e7-120">Header</span></span><br/> | <dl> <span data-ttu-id="225e7-121"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="225e7-121"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="225e7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="225e7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="225e7-123">X 檔案結構</span><span class="sxs-lookup"><span data-stu-id="225e7-123">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="225e7-124">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="225e7-124">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="225e7-125">DXFILE 常數</span><span class="sxs-lookup"><span data-stu-id="225e7-125">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
