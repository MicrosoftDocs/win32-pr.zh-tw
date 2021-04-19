---
description: 抓取具有指定名稱的資料物件。 已取代。
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'IDirectXFileEnumObject：： GetDataObjectByName 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985908"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="c5dcb-104">IDirectXFileEnumObject：： GetDataObjectByName 方法</span><span class="sxs-lookup"><span data-stu-id="c5dcb-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="c5dcb-105">抓取具有指定名稱的資料物件。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="c5dcb-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5dcb-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5dcb-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="c5dcb-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5dcb-109">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5dcb-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dcb-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dcb-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5dcb-111">所要求名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="c5dcb-112">*ppDataObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5dcb-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dcb-113">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5dcb-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="c5dcb-114">[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5dcb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5dcb-115">Return value</span></span>

<span data-ttu-id="c5dcb-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5dcb-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5dcb-117">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c5dcb-118">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="c5dcb-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5dcb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5dcb-119">Requirements</span></span>



| <span data-ttu-id="c5dcb-120">需求</span><span class="sxs-lookup"><span data-stu-id="c5dcb-120">Requirement</span></span> | <span data-ttu-id="c5dcb-121">值</span><span class="sxs-lookup"><span data-stu-id="c5dcb-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5dcb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c5dcb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c5dcb-123"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcb-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5dcb-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5dcb-124">Library</span></span><br/> | <dl> <span data-ttu-id="c5dcb-125"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcb-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5dcb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5dcb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5dcb-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="c5dcb-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 
