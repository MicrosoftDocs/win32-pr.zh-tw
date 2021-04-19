---
description: 從. x 檔案載入最上層資料。
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData：： LoadTopLevelData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974891"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="dd5ac-103">ID3DXLoadUserData：： LoadTopLevelData 方法</span><span class="sxs-lookup"><span data-stu-id="dd5ac-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="dd5ac-104">從. x 檔案載入最上層資料。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd5ac-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="dd5ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd5ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5ac-107">*pXofChildData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd5ac-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd5ac-108">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="dd5ac-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="dd5ac-109">. X 檔案資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="dd5ac-110">這是在 Dxfile 中定義。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd5ac-111">Return value</span></span>

<span data-ttu-id="dd5ac-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd5ac-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd5ac-113">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="dd5ac-114">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="dd5ac-115">否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dd5ac-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5ac-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd5ac-116">Requirements</span></span>



| <span data-ttu-id="dd5ac-117">需求</span><span class="sxs-lookup"><span data-stu-id="dd5ac-117">Requirement</span></span> | <span data-ttu-id="dd5ac-118">值</span><span class="sxs-lookup"><span data-stu-id="dd5ac-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5ac-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dd5ac-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dd5ac-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd5ac-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dd5ac-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd5ac-121">Library</span></span><br/> | <dl> <span data-ttu-id="dd5ac-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd5ac-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd5ac-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd5ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5ac-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="dd5ac-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




