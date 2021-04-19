---
description: 建立 DirectXFile 物件的實例。 已取代。
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: 'DirectXFileCreate 函式 (DXFile) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981816"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="b86d8-104">DirectXFileCreate 函式</span><span class="sxs-lookup"><span data-stu-id="b86d8-104">DirectXFileCreate function</span></span>

<span data-ttu-id="b86d8-105">建立 DirectXFile 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="b86d8-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="b86d8-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="b86d8-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="b86d8-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="b86d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="b86d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86d8-109">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="b86d8-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="b86d8-110">類型： **[ **LPDIRECTXFILE**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="b86d8-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="b86d8-111">[**IDirectXFile**](idirectxfile.md)介面指標的位址，表示已建立的 DirectXFile 物件。</span><span class="sxs-lookup"><span data-stu-id="b86d8-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b86d8-112">Return value</span></span>

<span data-ttu-id="b86d8-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b86d8-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b86d8-114">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b86d8-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b86d8-115">如果函式失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC，DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="b86d8-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86d8-116">備註</span><span class="sxs-lookup"><span data-stu-id="b86d8-116">Remarks</span></span>

<span data-ttu-id="b86d8-117">使用此函式之後，請使用 [**RegisterTemplates**](idirectxfile--registertemplates.md) 來註冊範本、使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 來建立列舉值物件，或使用 [**CreateSaveObject**](idirectxfile--createsaveobject.md) 來建立儲存物件。</span><span class="sxs-lookup"><span data-stu-id="b86d8-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86d8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b86d8-118">Requirements</span></span>



| <span data-ttu-id="b86d8-119">需求</span><span class="sxs-lookup"><span data-stu-id="b86d8-119">Requirement</span></span> | <span data-ttu-id="b86d8-120">值</span><span class="sxs-lookup"><span data-stu-id="b86d8-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b86d8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b86d8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b86d8-122"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="b86d8-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b86d8-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b86d8-123">Library</span></span><br/> | <dl> <span data-ttu-id="b86d8-124"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86d8-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="b86d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b86d8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b86d8-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86d8-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86d8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b86d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86d8-128">X 檔案函數</span><span class="sxs-lookup"><span data-stu-id="b86d8-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="b86d8-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="b86d8-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="b86d8-130">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="b86d8-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="b86d8-131">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="b86d8-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




