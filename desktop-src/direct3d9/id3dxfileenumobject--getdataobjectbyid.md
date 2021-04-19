---
description: 抓取具有指定之 GUID 的資料物件。
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject：： GetDataObjectById 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992729"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="a1a3b-103">ID3DXFileEnumObject：： GetDataObjectById 方法</span><span class="sxs-lookup"><span data-stu-id="a1a3b-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="a1a3b-104">抓取具有指定之 GUID 的資料物件。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1a3b-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="a1a3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1a3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a3b-107">*rguid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1a3b-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a3b-108">類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="a1a3b-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="a1a3b-109">參考要求的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="a1a3b-110">*ppDataObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1a3b-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a3b-111">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1a3b-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="a1a3b-112">[**ID3DXFileData**](id3dxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a3b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1a3b-113">Return value</span></span>

<span data-ttu-id="a1a3b-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1a3b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1a3b-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a1a3b-116">如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a3b-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1a3b-117">Remarks</span></span>

<span data-ttu-id="a1a3b-118">使用 [**ID3DXFileData：： GetId**](id3dxfiledata--getid.md) 方法，取得目前檔案資料物件的 GUID rguid。</span><span class="sxs-lookup"><span data-stu-id="a1a3b-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a3b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1a3b-119">Requirements</span></span>



| <span data-ttu-id="a1a3b-120">需求</span><span class="sxs-lookup"><span data-stu-id="a1a3b-120">Requirement</span></span> | <span data-ttu-id="a1a3b-121">值</span><span class="sxs-lookup"><span data-stu-id="a1a3b-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a3b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a1a3b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a3b-123"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a3b-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a1a3b-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1a3b-124">Library</span></span><br/> | <dl> <span data-ttu-id="a1a3b-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1a3b-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a1a3b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1a3b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a3b-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="a1a3b-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
