---
description: 抓取呈現介面的描述。
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap：： GetDesc 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696608"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="7d83b-103">ID3DXRenderToEnvMap：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="7d83b-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="7d83b-104">抓取呈現介面的描述。</span><span class="sxs-lookup"><span data-stu-id="7d83b-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d83b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d83b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7d83b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d83b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d83b-107">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d83b-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d83b-108">類型： **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d83b-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="7d83b-109">描述呈現介面之 [**D3DXRTE \_ DESC**](d3dxrte-desc.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d83b-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d83b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d83b-110">Return value</span></span>

<span data-ttu-id="7d83b-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d83b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d83b-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7d83b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7d83b-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7d83b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d83b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d83b-114">Requirements</span></span>



| <span data-ttu-id="7d83b-115">需求</span><span class="sxs-lookup"><span data-stu-id="7d83b-115">Requirement</span></span> | <span data-ttu-id="7d83b-116">值</span><span class="sxs-lookup"><span data-stu-id="7d83b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d83b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7d83b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7d83b-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d83b-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7d83b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d83b-119">Library</span></span><br/> | <dl> <span data-ttu-id="7d83b-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d83b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d83b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d83b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d83b-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="7d83b-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




