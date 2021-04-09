---
description: 建立列舉值物件。 已取代。
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile：： CreateEnumObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696776"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="3dd82-104">IDirectXFile：： CreateEnumObject 方法</span><span class="sxs-lookup"><span data-stu-id="3dd82-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="3dd82-105">建立列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="3dd82-105">Creates an enumerator object.</span></span> <span data-ttu-id="3dd82-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="3dd82-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd82-107">語法</span><span class="sxs-lookup"><span data-stu-id="3dd82-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="3dd82-108">參數</span><span class="sxs-lookup"><span data-stu-id="3dd82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd82-109">*pvSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dd82-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd82-110">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3dd82-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3dd82-111">其內容相依于 dwLoadOptions 值的資料指標</span><span class="sxs-lookup"><span data-stu-id="3dd82-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="3dd82-112">*dwLoadOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dd82-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd82-113">類型： **[ **DXFILELOADOPTIONS**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="3dd82-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="3dd82-114">指定資料來源的值。</span><span class="sxs-lookup"><span data-stu-id="3dd82-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="3dd82-115">這個值可以是 \_ [DXFILE 常數](dxfile.md)中的其中一個 DXFILELOAD xxx 旗標。</span><span class="sxs-lookup"><span data-stu-id="3dd82-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd82-116">*ppEnumObj* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="3dd82-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd82-117">類型： **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="3dd82-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="3dd82-118">[**IDirectXFileEnumObject**](idirectxfileenumobject.md)介面指標的位址，表示已建立的枚舉器物件。</span><span class="sxs-lookup"><span data-stu-id="3dd82-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd82-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dd82-119">Return value</span></span>

<span data-ttu-id="3dd82-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3dd82-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3dd82-121">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3dd82-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3dd82-122">如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC、DXFILEERR \_ BADFILEFLOATSIZE、DXFILEERR \_ BADFILETYPE、DXFILEERR \_ BADFILEVERSION、DXFILEERR \_ BADRESOURCE、DXFILEERR \_ BADVALUE、DXFILEERR \_ FILENOTFOUND、DXFILEERR \_ RESOURCENOTFOUND、DXFILEERR \_ URLNOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="3dd82-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd82-123">備註</span><span class="sxs-lookup"><span data-stu-id="3dd82-123">Remarks</span></span>

<span data-ttu-id="3dd82-124">使用這個方法之後，請使用其中一個 IDirectXFileEnumObject 方法來取出資料物件。</span><span class="sxs-lookup"><span data-stu-id="3dd82-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd82-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dd82-125">Requirements</span></span>



| <span data-ttu-id="3dd82-126">需求</span><span class="sxs-lookup"><span data-stu-id="3dd82-126">Requirement</span></span> | <span data-ttu-id="3dd82-127">值</span><span class="sxs-lookup"><span data-stu-id="3dd82-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd82-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3dd82-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3dd82-129"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd82-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dd82-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="3dd82-130">Library</span></span><br/> | <dl> <span data-ttu-id="3dd82-131"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dd82-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd82-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dd82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd82-133">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="3dd82-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
