---
description: 建立資料物件。 已取代。
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject：： CreateDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322847"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="935be-104">IDirectXFileSaveObject：： CreateDataObject 方法</span><span class="sxs-lookup"><span data-stu-id="935be-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="935be-105">建立資料物件。</span><span class="sxs-lookup"><span data-stu-id="935be-105">Creates a data object.</span></span> <span data-ttu-id="935be-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="935be-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="935be-107">語法</span><span class="sxs-lookup"><span data-stu-id="935be-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="935be-108">參數</span><span class="sxs-lookup"><span data-stu-id="935be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935be-109">*rguidTemplate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="935be-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-110">類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="935be-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="935be-111">代表資料物件之範本的 GUID。</span><span class="sxs-lookup"><span data-stu-id="935be-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="935be-112">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="935be-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-113">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="935be-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="935be-114">資料物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="935be-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="935be-115">如果物件沒有名稱，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="935be-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="935be-116">*pguid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="935be-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-117">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="935be-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="935be-118">代表資料物件之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="935be-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="935be-119">如果物件沒有 GUID，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="935be-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="935be-120">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="935be-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="935be-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="935be-122">資料物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="935be-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="935be-123">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="935be-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-124">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="935be-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="935be-125">包含所有必要成員資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="935be-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="935be-126">*ppDataObj* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="935be-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="935be-127">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="935be-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="935be-128">[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示所建立的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="935be-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="935be-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="935be-129">Return value</span></span>

<span data-ttu-id="935be-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="935be-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="935be-131">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="935be-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="935be-132">如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="935be-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="935be-133">備註</span><span class="sxs-lookup"><span data-stu-id="935be-133">Remarks</span></span>

<span data-ttu-id="935be-134">如果資料參考物件將參考資料物件，則 >szname 或 pguid 參數都必須為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="935be-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="935be-135">儲存這個方法所建立的資料之前，請先使用 [**IDirectXFileSaveObject：： SaveTemplates**](idirectxfilesaveobject--savetemplates.md) 方法儲存任何範本。</span><span class="sxs-lookup"><span data-stu-id="935be-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="935be-136">使用 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md) 方法儲存建立的資料。</span><span class="sxs-lookup"><span data-stu-id="935be-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="935be-137">如果您需要儲存選擇性資料，請在使用此方法之後，以及使用 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md)之前，使用 [**IDirectXFileData：： AddDataObject**](idirectxfiledata--adddataobject.md)方法。</span><span class="sxs-lookup"><span data-stu-id="935be-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="935be-138">如果物件有子物件，請在呼叫 **IDirectXFileSaveObject：： SaveData** 之前加入它們。</span><span class="sxs-lookup"><span data-stu-id="935be-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="935be-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="935be-139">Requirements</span></span>



| <span data-ttu-id="935be-140">需求</span><span class="sxs-lookup"><span data-stu-id="935be-140">Requirement</span></span> | <span data-ttu-id="935be-141">值</span><span class="sxs-lookup"><span data-stu-id="935be-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="935be-142">標頭</span><span class="sxs-lookup"><span data-stu-id="935be-142">Header</span></span><br/>  | <dl> <span data-ttu-id="935be-143"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="935be-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="935be-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="935be-144">Library</span></span><br/> | <dl> <span data-ttu-id="935be-145"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="935be-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935be-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="935be-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935be-147">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="935be-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="935be-148">**IDirectXFileData::AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="935be-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="935be-149">**IDirectXFileSaveObject：： SaveData**</span><span class="sxs-lookup"><span data-stu-id="935be-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="935be-150">**IDirectXFileSaveObject::SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="935be-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
