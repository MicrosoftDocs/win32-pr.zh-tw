---
description: 將範本儲存至 DirectX 檔案。 已取代。
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject：： SaveTemplates 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322844"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="3725d-104">IDirectXFileSaveObject：： SaveTemplates 方法</span><span class="sxs-lookup"><span data-stu-id="3725d-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="3725d-105">將範本儲存至 DirectX 檔案。</span><span class="sxs-lookup"><span data-stu-id="3725d-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="3725d-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="3725d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3725d-107">語法</span><span class="sxs-lookup"><span data-stu-id="3725d-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="3725d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3725d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3725d-109">*cTemplates* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3725d-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3725d-110">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3725d-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3725d-111">要儲存的範本總數。</span><span class="sxs-lookup"><span data-stu-id="3725d-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="3725d-112">*ppguidTemplates* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3725d-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3725d-113">類型： **Const [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="3725d-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="3725d-114">要儲存之所有範本的 Guid 陣列指標位址。</span><span class="sxs-lookup"><span data-stu-id="3725d-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3725d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3725d-115">Return value</span></span>

<span data-ttu-id="3725d-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3725d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3725d-117">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3725d-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3725d-118">如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="3725d-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3725d-119">備註</span><span class="sxs-lookup"><span data-stu-id="3725d-119">Remarks</span></span>

<span data-ttu-id="3725d-120">下列程式碼片段提供 **IDirectXFileSaveObject：： SaveTemplates** 的範例呼叫，以及 ppguidTemplates 點的陣列範例內容。</span><span class="sxs-lookup"><span data-stu-id="3725d-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="3725d-121">使用這個方法來儲存範本之後，請使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立資料物件。</span><span class="sxs-lookup"><span data-stu-id="3725d-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3725d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3725d-122">Requirements</span></span>



| <span data-ttu-id="3725d-123">需求</span><span class="sxs-lookup"><span data-stu-id="3725d-123">Requirement</span></span> | <span data-ttu-id="3725d-124">值</span><span class="sxs-lookup"><span data-stu-id="3725d-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3725d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3725d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3725d-126"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="3725d-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3725d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3725d-127">Library</span></span><br/> | <dl> <span data-ttu-id="3725d-128"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3725d-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3725d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3725d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3725d-130">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="3725d-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="3725d-131">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="3725d-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
