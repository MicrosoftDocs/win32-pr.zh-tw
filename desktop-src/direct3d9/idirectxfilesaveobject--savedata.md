---
description: 將資料物件和其子系儲存至 DirectX 檔案。 已取代。
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'IDirectXFileSaveObject：： SaveData 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997243"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="c7997-104">IDirectXFileSaveObject：： SaveData 方法</span><span class="sxs-lookup"><span data-stu-id="c7997-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="c7997-105">將資料物件和其子系儲存至 DirectX 檔案。</span><span class="sxs-lookup"><span data-stu-id="c7997-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="c7997-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="c7997-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7997-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7997-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="c7997-108">參數</span><span class="sxs-lookup"><span data-stu-id="c7997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7997-109">*pDataObj* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7997-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7997-110">類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="c7997-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="c7997-111">[**IDirectXFileData**](idirectxfiledata.md)介面的指標，代表要儲存的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="c7997-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7997-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7997-112">Return value</span></span>

<span data-ttu-id="c7997-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7997-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7997-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c7997-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c7997-115">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADARRAYSIZE，DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="c7997-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7997-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7997-116">Requirements</span></span>



| <span data-ttu-id="c7997-117">需求</span><span class="sxs-lookup"><span data-stu-id="c7997-117">Requirement</span></span> | <span data-ttu-id="c7997-118">值</span><span class="sxs-lookup"><span data-stu-id="c7997-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7997-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c7997-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c7997-120"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7997-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7997-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7997-121">Library</span></span><br/> | <dl> <span data-ttu-id="c7997-122"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7997-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7997-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7997-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7997-124">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="c7997-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




