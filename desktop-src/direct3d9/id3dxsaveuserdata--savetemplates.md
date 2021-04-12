---
description: 使用者用來儲存. x 檔案範本的回呼。
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'ID3DXSaveUserData：： SaveTemplates 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946246"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="7d326-103">ID3DXSaveUserData：： SaveTemplates 方法</span><span class="sxs-lookup"><span data-stu-id="7d326-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="7d326-104">使用者用來儲存. x 檔案範本的回呼。</span><span class="sxs-lookup"><span data-stu-id="7d326-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d326-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d326-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="7d326-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d326-107">*pXofSave* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d326-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d326-108">類型： **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="7d326-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="7d326-109">. X 檔儲存物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7d326-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="7d326-110">請勿使用此參數來加入資料物件。</span><span class="sxs-lookup"><span data-stu-id="7d326-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="7d326-111">請參閱 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)。</span><span class="sxs-lookup"><span data-stu-id="7d326-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d326-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d326-112">Return value</span></span>

<span data-ttu-id="7d326-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d326-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d326-114">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="7d326-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7d326-115">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7d326-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7d326-116">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d326-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d326-117">備註</span><span class="sxs-lookup"><span data-stu-id="7d326-117">Remarks</span></span>

<span data-ttu-id="7d326-118">[**ID3DXSaveUserData：： RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) 和 **ID3DXSaveUserData：： SaveTemplates** 提供一種機制，可將範本加入至用來儲存使用者資料的. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d326-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d326-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d326-119">Requirements</span></span>



| <span data-ttu-id="7d326-120">需求</span><span class="sxs-lookup"><span data-stu-id="7d326-120">Requirement</span></span> | <span data-ttu-id="7d326-121">值</span><span class="sxs-lookup"><span data-stu-id="7d326-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d326-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7d326-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7d326-123"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d326-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7d326-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d326-124">Library</span></span><br/> | <dl> <span data-ttu-id="7d326-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d326-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d326-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d326-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d326-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="7d326-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
