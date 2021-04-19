---
description: 抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。 已取代。
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'IDirectXFileData：： GetNextObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997412"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="9a661-104">IDirectXFileData：： GetNextObject 方法</span><span class="sxs-lookup"><span data-stu-id="9a661-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="9a661-105">抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。</span><span class="sxs-lookup"><span data-stu-id="9a661-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="9a661-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="9a661-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a661-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a661-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="9a661-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a661-109">*ppChildObj* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="9a661-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9a661-110">類型： **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a661-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="9a661-111">[**IDirectXFileObject**](idirectxfileobject.md)介面指標的位址，表示傳回的子物件的檔案物件介面。</span><span class="sxs-lookup"><span data-stu-id="9a661-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a661-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a661-112">Return value</span></span>

<span data-ttu-id="9a661-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a661-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a661-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9a661-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="9a661-115">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOMOREOBJECTS。</span><span class="sxs-lookup"><span data-stu-id="9a661-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a661-116">備註</span><span class="sxs-lookup"><span data-stu-id="9a661-116">Remarks</span></span>

<span data-ttu-id="9a661-117">若要判斷抓取的物件類型，請使用 QueryInterface 來查詢已抓取的物件，以支援 [**IDirectXFileData**](idirectxfiledata.md)、 [**IDirectXFileDataReference**](idirectxfiledatareference.md)或 [**IDirectXFileBinary**](idirectxfilebinary.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="9a661-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="9a661-118">支援的介面表示 (資料、資料參考或二進位) 的物件類型。</span><span class="sxs-lookup"><span data-stu-id="9a661-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a661-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a661-119">Requirements</span></span>



| <span data-ttu-id="9a661-120">需求</span><span class="sxs-lookup"><span data-stu-id="9a661-120">Requirement</span></span> | <span data-ttu-id="9a661-121">值</span><span class="sxs-lookup"><span data-stu-id="9a661-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a661-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9a661-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a661-123"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a661-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a661-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a661-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a661-125"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a661-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a661-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a661-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a661-127">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="9a661-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="9a661-128">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="9a661-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="9a661-129">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="9a661-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




