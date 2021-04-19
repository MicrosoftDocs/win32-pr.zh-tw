---
description: 將資料物件新增為 ID3DXFileSaveData 物件的子系。
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject：： AddDataObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981826"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="fd9bf-103">ID3DXFileSaveObject：： AddDataObject 方法</span><span class="sxs-lookup"><span data-stu-id="fd9bf-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="fd9bf-104">將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件的子系。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="fd9bf-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fd9bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd9bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9bf-107">*rguidTemplate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-108">類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="fd9bf-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="fd9bf-109">代表資料物件之範本的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="fd9bf-110">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd9bf-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd9bf-112">資料物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="fd9bf-113">如果物件沒有名稱，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="fd9bf-114">*pId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-115">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd9bf-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="fd9bf-116">代表資料物件之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="fd9bf-117">如果物件沒有 GUID，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="fd9bf-118">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-119">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd9bf-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd9bf-120">資料物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fd9bf-121">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-122">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd9bf-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd9bf-123">包含資料物件中所有必要資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="fd9bf-124">*ppObj* \[在中，retval\]</span><span class="sxs-lookup"><span data-stu-id="fd9bf-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9bf-125">類型： **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fd9bf-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="fd9bf-126">[**ID3DXFileSaveData**](id3dxfilesavedata.md)介面指標的位址，代表將加入資料物件的檔案資料節點。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9bf-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd9bf-127">Return value</span></span>

<span data-ttu-id="fd9bf-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd9bf-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd9bf-129">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fd9bf-130">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT、DXFILEERR \_ BADVALUE、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9bf-131">備註</span><span class="sxs-lookup"><span data-stu-id="fd9bf-131">Remarks</span></span>

<span data-ttu-id="fd9bf-132">如果資料參考物件將參考資料物件，則 >szname 或 pId 參數都必須為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="fd9bf-133">使用 [**ID3DXFileSaveObject：： save**](id3dxfilesaveobject--save.md) 方法將建立的資料儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="fd9bf-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9bf-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd9bf-134">Requirements</span></span>



| <span data-ttu-id="fd9bf-135">需求</span><span class="sxs-lookup"><span data-stu-id="fd9bf-135">Requirement</span></span> | <span data-ttu-id="fd9bf-136">值</span><span class="sxs-lookup"><span data-stu-id="fd9bf-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9bf-137">標頭</span><span class="sxs-lookup"><span data-stu-id="fd9bf-137">Header</span></span><br/>  | <dl> <span data-ttu-id="fd9bf-138"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd9bf-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fd9bf-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd9bf-139">Library</span></span><br/> | <dl> <span data-ttu-id="fd9bf-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd9bf-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fd9bf-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd9bf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9bf-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="fd9bf-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
