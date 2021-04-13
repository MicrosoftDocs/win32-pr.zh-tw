---
description: 抓取 DirectX 檔案中的下一個最上層物件。 已取代。
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'IDirectXFileEnumObject：： GetNextDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322668"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="e1bb4-104">IDirectXFileEnumObject：： GetNextDataObject 方法</span><span class="sxs-lookup"><span data-stu-id="e1bb4-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="e1bb4-105">抓取 DirectX 檔案中的下一個最上層物件。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="e1bb4-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bb4-107">語法</span><span class="sxs-lookup"><span data-stu-id="e1bb4-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="e1bb4-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1bb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1bb4-109">*ppDataObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e1bb4-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1bb4-110">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1bb4-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="e1bb4-111">[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1bb4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1bb4-112">Return value</span></span>

<span data-ttu-id="e1bb4-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1bb4-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="e1bb4-115">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE、DXFILEERR \_ NOMOREOBJECTS</span><span class="sxs-lookup"><span data-stu-id="e1bb4-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bb4-116">備註</span><span class="sxs-lookup"><span data-stu-id="e1bb4-116">Remarks</span></span>

<span data-ttu-id="e1bb4-117">最上層物件一律是資料物件。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="e1bb4-118">資料參考物件和二進位物件只能是資料物件的子系。</span><span class="sxs-lookup"><span data-stu-id="e1bb4-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bb4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1bb4-119">Requirements</span></span>



| <span data-ttu-id="e1bb4-120">需求</span><span class="sxs-lookup"><span data-stu-id="e1bb4-120">Requirement</span></span> | <span data-ttu-id="e1bb4-121">值</span><span class="sxs-lookup"><span data-stu-id="e1bb4-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bb4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e1bb4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e1bb4-123"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1bb4-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1bb4-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1bb4-124">Library</span></span><br/> | <dl> <span data-ttu-id="e1bb4-125"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1bb4-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1bb4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1bb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bb4-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="e1bb4-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 




