---
description: 抓取具有指定之 GUID 的資料物件。 已取代。
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'IDirectXFileEnumObject：： GetDataObjectById 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976682"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="cb78b-104">IDirectXFileEnumObject：： GetDataObjectById 方法</span><span class="sxs-lookup"><span data-stu-id="cb78b-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="cb78b-105">抓取具有指定之 GUID 的資料物件。</span><span class="sxs-lookup"><span data-stu-id="cb78b-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="cb78b-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="cb78b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb78b-107">語法</span><span class="sxs-lookup"><span data-stu-id="cb78b-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="cb78b-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb78b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb78b-109">*rguid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb78b-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb78b-110">類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="cb78b-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="cb78b-111">參考要求的 GUID。</span><span class="sxs-lookup"><span data-stu-id="cb78b-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="cb78b-112">*ppDataObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb78b-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb78b-113">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb78b-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="cb78b-114">[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="cb78b-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb78b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb78b-115">Return value</span></span>

<span data-ttu-id="cb78b-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb78b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb78b-117">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="cb78b-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="cb78b-118">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="cb78b-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb78b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb78b-119">Requirements</span></span>



| <span data-ttu-id="cb78b-120">需求</span><span class="sxs-lookup"><span data-stu-id="cb78b-120">Requirement</span></span> | <span data-ttu-id="cb78b-121">值</span><span class="sxs-lookup"><span data-stu-id="cb78b-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb78b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cb78b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cb78b-123"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb78b-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb78b-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb78b-124">Library</span></span><br/> | <dl> <span data-ttu-id="cb78b-125"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb78b-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb78b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb78b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb78b-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="cb78b-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
