---
description: 將資料物件新增為子物件。 已取代。
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'IDirectXFileData：： AddDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323136"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="e2cd4-104">IDirectXFileData：： AddDataObject 方法</span><span class="sxs-lookup"><span data-stu-id="e2cd4-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="e2cd4-105">將資料物件新增為子物件。</span><span class="sxs-lookup"><span data-stu-id="e2cd4-105">Adds a data object as a child object.</span></span> <span data-ttu-id="e2cd4-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="e2cd4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2cd4-107">語法</span><span class="sxs-lookup"><span data-stu-id="e2cd4-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="e2cd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2cd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cd4-109">*pDataObj* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2cd4-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2cd4-110">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="e2cd4-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="e2cd4-111">[**IDirectXFileData**](idirectxfiledata.md)介面的指標，代表要新增為子物件的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="e2cd4-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2cd4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2cd4-112">Return value</span></span>

<span data-ttu-id="e2cd4-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2cd4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2cd4-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e2cd4-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="e2cd4-115">如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="e2cd4-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="e2cd4-116">備註</span><span class="sxs-lookup"><span data-stu-id="e2cd4-116">Remarks</span></span>

<span data-ttu-id="e2cd4-117">在呼叫這個方法之前，請使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 [**IDirectXFileData**](idirectxfiledata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e2cd4-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2cd4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2cd4-118">Requirements</span></span>



| <span data-ttu-id="e2cd4-119">需求</span><span class="sxs-lookup"><span data-stu-id="e2cd4-119">Requirement</span></span> | <span data-ttu-id="e2cd4-120">值</span><span class="sxs-lookup"><span data-stu-id="e2cd4-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cd4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e2cd4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e2cd4-122"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd4-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2cd4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2cd4-123">Library</span></span><br/> | <dl> <span data-ttu-id="e2cd4-124"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd4-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2cd4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2cd4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cd4-126">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="e2cd4-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="e2cd4-127">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="e2cd4-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




