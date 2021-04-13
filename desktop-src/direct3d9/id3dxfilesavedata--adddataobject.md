---
description: 將資料物件新增為 ID3DXFileSaveData 檔資料節點的子系。
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData：： AddDataObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323064"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="02a55-103">ID3DXFileSaveData：： AddDataObject 方法</span><span class="sxs-lookup"><span data-stu-id="02a55-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="02a55-104">將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的子系。</span><span class="sxs-lookup"><span data-stu-id="02a55-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a55-105">語法</span><span class="sxs-lookup"><span data-stu-id="02a55-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="02a55-106">參數</span><span class="sxs-lookup"><span data-stu-id="02a55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a55-107">*rguidTemplate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a55-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-108">類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="02a55-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="02a55-109">代表資料物件之範本的 GUID。</span><span class="sxs-lookup"><span data-stu-id="02a55-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="02a55-110">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a55-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a55-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a55-112">要加入之資料物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="02a55-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="02a55-113">如果物件沒有名稱，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="02a55-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="02a55-114">*pId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a55-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-115">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="02a55-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="02a55-116">代表資料物件之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="02a55-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="02a55-117">資料物件必須已向 [**ID3DXFile：： RegisterTemplates**](id3dxfile--registertemplates.md) 或 [**ID3DXFile：： RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)註冊。</span><span class="sxs-lookup"><span data-stu-id="02a55-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="02a55-118">如果物件沒有 GUID，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="02a55-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="02a55-119">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a55-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-120">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a55-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a55-121">資料物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="02a55-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="02a55-122">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02a55-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-123">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02a55-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02a55-124">包含資料物件中所有必要資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="02a55-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="02a55-125">*ppObj* \[在中，retval\]</span><span class="sxs-lookup"><span data-stu-id="02a55-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="02a55-126">類型： **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="02a55-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="02a55-127">[**ID3DXFileSaveData**](id3dxfilesavedata.md)介面指標的位址，代表將加入資料物件的檔案資料節點。</span><span class="sxs-lookup"><span data-stu-id="02a55-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a55-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="02a55-128">Return value</span></span>

<span data-ttu-id="02a55-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02a55-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02a55-130">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="02a55-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="02a55-131">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、D3DXFERR \_ BADVALUE、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="02a55-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a55-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a55-132">Requirements</span></span>



| <span data-ttu-id="02a55-133">需求</span><span class="sxs-lookup"><span data-stu-id="02a55-133">Requirement</span></span> | <span data-ttu-id="02a55-134">值</span><span class="sxs-lookup"><span data-stu-id="02a55-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02a55-135">標頭</span><span class="sxs-lookup"><span data-stu-id="02a55-135">Header</span></span><br/>  | <dl> <span data-ttu-id="02a55-136"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="02a55-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="02a55-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="02a55-137">Library</span></span><br/> | <dl> <span data-ttu-id="02a55-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02a55-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="02a55-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a55-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a55-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="02a55-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
