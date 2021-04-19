---
description: 解析資料參考。 已取代。
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'IDirectXFileDataReference：： Resolve 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976725"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="12bad-104">IDirectXFileDataReference：： Resolve 方法</span><span class="sxs-lookup"><span data-stu-id="12bad-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="12bad-105">解析資料參考。</span><span class="sxs-lookup"><span data-stu-id="12bad-105">Resolves data references.</span></span> <span data-ttu-id="12bad-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="12bad-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bad-107">語法</span><span class="sxs-lookup"><span data-stu-id="12bad-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="12bad-108">參數</span><span class="sxs-lookup"><span data-stu-id="12bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bad-109">*ppDataObj* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="12bad-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="12bad-110">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="12bad-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="12bad-111">[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="12bad-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bad-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="12bad-112">Return value</span></span>

<span data-ttu-id="12bad-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12bad-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12bad-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="12bad-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="12bad-115">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="12bad-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="12bad-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="12bad-116">Requirements</span></span>



| <span data-ttu-id="12bad-117">需求</span><span class="sxs-lookup"><span data-stu-id="12bad-117">Requirement</span></span> | <span data-ttu-id="12bad-118">值</span><span class="sxs-lookup"><span data-stu-id="12bad-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12bad-119">標頭</span><span class="sxs-lookup"><span data-stu-id="12bad-119">Header</span></span><br/>  | <dl> <span data-ttu-id="12bad-120"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="12bad-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="12bad-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="12bad-121">Library</span></span><br/> | <dl> <span data-ttu-id="12bad-122"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="12bad-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12bad-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12bad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bad-124">IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="12bad-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




