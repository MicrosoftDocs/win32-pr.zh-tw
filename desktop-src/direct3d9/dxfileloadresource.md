---
description: 識別資源資料。 已取代。
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: 'DXFILELOADRESOURCE 結構 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988200"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="af85e-104">DXFILELOADRESOURCE 結構</span><span class="sxs-lookup"><span data-stu-id="af85e-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="af85e-105">識別資源資料。</span><span class="sxs-lookup"><span data-stu-id="af85e-105">Identifies resource data.</span></span> <span data-ttu-id="af85e-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="af85e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="af85e-107">語法</span><span class="sxs-lookup"><span data-stu-id="af85e-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="af85e-108">成員</span><span class="sxs-lookup"><span data-stu-id="af85e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="af85e-109">**hModule**</span><span class="sxs-lookup"><span data-stu-id="af85e-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="af85e-110">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af85e-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af85e-111">模組的控制碼，其中包含要載入的資源。</span><span class="sxs-lookup"><span data-stu-id="af85e-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="af85e-112">如果這個成員是 **Null**，則資源必須附加至將使用它的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="af85e-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="af85e-113">**lpName**</span><span class="sxs-lookup"><span data-stu-id="af85e-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="af85e-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af85e-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af85e-115">指定要載入之資源名稱的字串指標。</span><span class="sxs-lookup"><span data-stu-id="af85e-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="af85e-116">例如，如果資源是網格，則這個成員應指定網格檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="af85e-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="af85e-117">**lpType**</span><span class="sxs-lookup"><span data-stu-id="af85e-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="af85e-118">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af85e-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af85e-119">字串的指標，指定識別資源的使用者定義型別。</span><span class="sxs-lookup"><span data-stu-id="af85e-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af85e-120">備註</span><span class="sxs-lookup"><span data-stu-id="af85e-120">Remarks</span></span>

<span data-ttu-id="af85e-121">當應用程式使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 方法並指定 DXFILELOAD FROMRESOURCE 時，此結構會識別要載入的資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="af85e-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="af85e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="af85e-122">Requirements</span></span>



| <span data-ttu-id="af85e-123">需求</span><span class="sxs-lookup"><span data-stu-id="af85e-123">Requirement</span></span> | <span data-ttu-id="af85e-124">值</span><span class="sxs-lookup"><span data-stu-id="af85e-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af85e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="af85e-125">Header</span></span><br/> | <dl> <span data-ttu-id="af85e-126"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="af85e-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af85e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af85e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af85e-128">X 檔案結構</span><span class="sxs-lookup"><span data-stu-id="af85e-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="af85e-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="af85e-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="af85e-130">DXFILE 常數</span><span class="sxs-lookup"><span data-stu-id="af85e-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
