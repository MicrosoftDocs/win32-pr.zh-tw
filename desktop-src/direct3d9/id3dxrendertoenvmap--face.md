---
description: 起始每個環境圖臉部的繪圖。
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap：：臉部方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696840"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="3c101-103">ID3DXRenderToEnvMap：：臉部方法</span><span class="sxs-lookup"><span data-stu-id="3c101-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="3c101-104">起始每個環境圖臉部的繪圖。</span><span class="sxs-lookup"><span data-stu-id="3c101-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c101-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c101-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="3c101-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c101-107">*臉部* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c101-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c101-108">類型： **[ **D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="3c101-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="3c101-109">環境 cube 對應的第一個臉部。</span><span class="sxs-lookup"><span data-stu-id="3c101-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="3c101-110">請參閱 [**D3DCUBEMAP \_ 臉部**](./d3dcubemap-faces.md)。</span><span class="sxs-lookup"><span data-stu-id="3c101-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c101-111">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c101-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c101-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c101-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c101-113">一或多個 [D3DX \_ 篩選](d3dx-filter.md) 旗標的有效組合。</span><span class="sxs-lookup"><span data-stu-id="3c101-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c101-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c101-114">Return value</span></span>

<span data-ttu-id="3c101-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c101-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c101-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3c101-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c101-117">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="3c101-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c101-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c101-118">Remarks</span></span>

<span data-ttu-id="3c101-119">您必須針對每個環境對應類型呼叫這個方法一次。</span><span class="sxs-lookup"><span data-stu-id="3c101-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="3c101-120">唯一的例外狀況是三次的環境對應，需要呼叫此方法六次，D3DCUBEMAP 臉部中的每個臉部 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3c101-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="3c101-121">如需詳細資訊，請參閱 [ (Direct3D 9) 的環境對應 ](environment-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="3c101-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c101-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c101-122">Requirements</span></span>



| <span data-ttu-id="3c101-123">需求</span><span class="sxs-lookup"><span data-stu-id="3c101-123">Requirement</span></span> | <span data-ttu-id="3c101-124">值</span><span class="sxs-lookup"><span data-stu-id="3c101-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c101-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3c101-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3c101-126"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c101-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3c101-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c101-127">Library</span></span><br/> | <dl> <span data-ttu-id="3c101-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c101-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c101-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c101-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c101-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="3c101-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
