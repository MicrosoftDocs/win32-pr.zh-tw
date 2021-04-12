---
description: 識別記憶體資料。
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: 'D3DXF_FILELOADMEMORY 結構 (D3dx9xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946100"
---
# <a name="d3dxf_fileloadmemory-structure"></a><span data-ttu-id="10c3a-103">D3DXF \_ FILELOADMEMORY 結構</span><span class="sxs-lookup"><span data-stu-id="10c3a-103">D3DXF\_FILELOADMEMORY structure</span></span>

<span data-ttu-id="10c3a-104">識別記憶體資料。</span><span class="sxs-lookup"><span data-stu-id="10c3a-104">Identifies memory data.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="10c3a-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a><span data-ttu-id="10c3a-106">成員</span><span class="sxs-lookup"><span data-stu-id="10c3a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="10c3a-107">**lpMemory**</span><span class="sxs-lookup"><span data-stu-id="10c3a-107">**lpMemory**</span></span>
</dt> <dd>

<span data-ttu-id="10c3a-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c3a-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="10c3a-109">要載入之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="10c3a-109">Pointer to a block of memory to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="10c3a-110">**dSize**</span><span class="sxs-lookup"><span data-stu-id="10c3a-110">**dSize**</span></span>
</dt> <dd>

<span data-ttu-id="10c3a-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c3a-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="10c3a-112">要載入之記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="10c3a-112">Size of the block of memory to be loaded, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10c3a-113">備註</span><span class="sxs-lookup"><span data-stu-id="10c3a-113">Remarks</span></span>

<span data-ttu-id="10c3a-114">當應用程式使用 [**CreateEnumObject**](id3dxfile--createenumobject.md) 方法並指定 D3DXF \_ FILELOAD FROMMEMORY 旗標時，此結構會識別要從記憶體載入的資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="10c3a-114">This structure identifies data to be loaded from memory when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the D3DXF\_FILELOAD\_FROMMEMORY flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c3a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10c3a-115">Requirements</span></span>



| <span data-ttu-id="10c3a-116">需求</span><span class="sxs-lookup"><span data-stu-id="10c3a-116">Requirement</span></span> | <span data-ttu-id="10c3a-117">值</span><span class="sxs-lookup"><span data-stu-id="10c3a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10c3a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="10c3a-118">Header</span></span><br/> | <dl> <span data-ttu-id="10c3a-119"><dt>D3dx9xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="10c3a-119"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c3a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c3a-121">D3DX X 檔案結構</span><span class="sxs-lookup"><span data-stu-id="10c3a-121">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
