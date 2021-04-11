---
description: 建立二進位物件，並將它新增為子物件。 已取代。
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'IDirectXFileData：： AddBinaryObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196187"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="65ddd-104">IDirectXFileData：： AddBinaryObject 方法</span><span class="sxs-lookup"><span data-stu-id="65ddd-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="65ddd-105">建立二進位物件，並將它新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="65ddd-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="65ddd-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="65ddd-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ddd-107">語法</span><span class="sxs-lookup"><span data-stu-id="65ddd-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="65ddd-108">參數</span><span class="sxs-lookup"><span data-stu-id="65ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ddd-109">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65ddd-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ddd-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65ddd-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65ddd-111">物件名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="65ddd-111">Pointer to the name of the object.</span></span> <span data-ttu-id="65ddd-112">如果物件不需要名稱，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="65ddd-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="65ddd-113">*pguid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65ddd-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ddd-114">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="65ddd-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="65ddd-115">代表物件之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="65ddd-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="65ddd-116">如果物件不需要 GUID，請指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="65ddd-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="65ddd-117">*szMimeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65ddd-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ddd-118">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65ddd-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65ddd-119">物件之 MIME 類型的指標。</span><span class="sxs-lookup"><span data-stu-id="65ddd-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="65ddd-120">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65ddd-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ddd-121">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65ddd-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65ddd-122">物件資料的指標。</span><span class="sxs-lookup"><span data-stu-id="65ddd-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="65ddd-123">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65ddd-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ddd-124">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65ddd-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65ddd-125">PvData 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="65ddd-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ddd-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="65ddd-126">Return value</span></span>

<span data-ttu-id="65ddd-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65ddd-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65ddd-128">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="65ddd-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="65ddd-129">如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="65ddd-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="65ddd-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="65ddd-130">Requirements</span></span>



| <span data-ttu-id="65ddd-131">需求</span><span class="sxs-lookup"><span data-stu-id="65ddd-131">Requirement</span></span> | <span data-ttu-id="65ddd-132">值</span><span class="sxs-lookup"><span data-stu-id="65ddd-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65ddd-133">標頭</span><span class="sxs-lookup"><span data-stu-id="65ddd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="65ddd-134"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="65ddd-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="65ddd-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="65ddd-135">Library</span></span><br/> | <dl> <span data-ttu-id="65ddd-136"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="65ddd-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ddd-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65ddd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ddd-138">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="65ddd-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="65ddd-139">**IDirectXFileBinary::GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="65ddd-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
