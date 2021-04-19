---
description: 從. x 檔案載入網格子資料。
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'ID3DXLoadUserData：： LoadMeshChildData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106995896"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="2a03a-103">ID3DXLoadUserData：： LoadMeshChildData 方法</span><span class="sxs-lookup"><span data-stu-id="2a03a-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="2a03a-104">從. x 檔案載入網格子資料。</span><span class="sxs-lookup"><span data-stu-id="2a03a-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a03a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a03a-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="2a03a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a03a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a03a-107">*pMeshContainer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a03a-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a03a-108">類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="2a03a-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="2a03a-109">網格容器的指標。</span><span class="sxs-lookup"><span data-stu-id="2a03a-109">Pointer to a mesh container.</span></span> <span data-ttu-id="2a03a-110">請參閱 [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="2a03a-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a03a-111">*pXofChildData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a03a-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a03a-112">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="2a03a-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="2a03a-113">. X 檔案資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2a03a-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="2a03a-114">這是在 Dxfile 中定義。</span><span class="sxs-lookup"><span data-stu-id="2a03a-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a03a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a03a-115">Return value</span></span>

<span data-ttu-id="2a03a-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a03a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a03a-117">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="2a03a-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="2a03a-118">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2a03a-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="2a03a-119">否則，請將方法程式設計成從 D3DERR 或 D3DXERR 傳回適當的錯誤訊息，因為這會導致 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 也失敗，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a03a-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a03a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a03a-120">Requirements</span></span>



| <span data-ttu-id="2a03a-121">需求</span><span class="sxs-lookup"><span data-stu-id="2a03a-121">Requirement</span></span> | <span data-ttu-id="2a03a-122">值</span><span class="sxs-lookup"><span data-stu-id="2a03a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a03a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2a03a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2a03a-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a03a-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2a03a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a03a-125">Library</span></span><br/> | <dl> <span data-ttu-id="2a03a-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a03a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a03a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a03a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a03a-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="2a03a-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




