---
description: 識別資源資料。
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: 'D3DXF_FILELOADRESOURCE 結構 (D3dx9xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981829"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="3f641-103">D3DXF \_ FILELOADRESOURCE 結構</span><span class="sxs-lookup"><span data-stu-id="3f641-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="3f641-104">識別資源資料。</span><span class="sxs-lookup"><span data-stu-id="3f641-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f641-105">語法</span><span class="sxs-lookup"><span data-stu-id="3f641-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="3f641-106">成員</span><span class="sxs-lookup"><span data-stu-id="3f641-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f641-107">**hModule**</span><span class="sxs-lookup"><span data-stu-id="3f641-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="3f641-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f641-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f641-109">模組的控制碼，其中包含要載入的資源。</span><span class="sxs-lookup"><span data-stu-id="3f641-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="3f641-110">如果這個成員是 **Null**，則資源必須附加至將使用它的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="3f641-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="3f641-111">**lpName**</span><span class="sxs-lookup"><span data-stu-id="3f641-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="3f641-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f641-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f641-113">指定要載入之資源名稱的字串指標。</span><span class="sxs-lookup"><span data-stu-id="3f641-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="3f641-114">例如，如果資源是網格，則這個成員應指定網格檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f641-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="3f641-115">**lpType**</span><span class="sxs-lookup"><span data-stu-id="3f641-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="3f641-116">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f641-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f641-117">字串的指標，指定識別資源的使用者定義型別。</span><span class="sxs-lookup"><span data-stu-id="3f641-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f641-118">備註</span><span class="sxs-lookup"><span data-stu-id="3f641-118">Remarks</span></span>

<span data-ttu-id="3f641-119">當應用程式使用 [**CreateEnumObject**](id3dxfile--createenumobject.md) 方法並指定 [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) 旗標時，此結構會識別要載入的資源。</span><span class="sxs-lookup"><span data-stu-id="3f641-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f641-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f641-120">Requirements</span></span>



| <span data-ttu-id="3f641-121">需求</span><span class="sxs-lookup"><span data-stu-id="3f641-121">Requirement</span></span> | <span data-ttu-id="3f641-122">值</span><span class="sxs-lookup"><span data-stu-id="3f641-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f641-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3f641-123">Header</span></span><br/> | <dl> <span data-ttu-id="3f641-124"><dt>D3dx9xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f641-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f641-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f641-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f641-126">D3DX X 檔案結構</span><span class="sxs-lookup"><span data-stu-id="3f641-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
