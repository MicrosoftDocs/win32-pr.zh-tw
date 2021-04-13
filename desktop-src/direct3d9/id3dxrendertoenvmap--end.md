---
description: 還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap：： End 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322803"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="33f1c-103">ID3DXRenderToEnvMap：： End 方法</span><span class="sxs-lookup"><span data-stu-id="33f1c-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="33f1c-104">還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。</span><span class="sxs-lookup"><span data-stu-id="33f1c-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="33f1c-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="33f1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="33f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f1c-107">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33f1c-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33f1c-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33f1c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33f1c-109">一或多個 [D3DX \_ 篩選](d3dx-filter.md) 旗標的有效組合。</span><span class="sxs-lookup"><span data-stu-id="33f1c-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f1c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="33f1c-110">Return value</span></span>

<span data-ttu-id="33f1c-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33f1c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33f1c-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="33f1c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33f1c-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="33f1c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f1c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="33f1c-114">Requirements</span></span>



| <span data-ttu-id="33f1c-115">需求</span><span class="sxs-lookup"><span data-stu-id="33f1c-115">Requirement</span></span> | <span data-ttu-id="33f1c-116">值</span><span class="sxs-lookup"><span data-stu-id="33f1c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33f1c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="33f1c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="33f1c-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="33f1c-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="33f1c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="33f1c-119">Library</span></span><br/> | <dl> <span data-ttu-id="33f1c-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="33f1c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33f1c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f1c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f1c-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="33f1c-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="33f1c-123">**ID3DXRenderToEnvMap：：臉部**</span><span class="sxs-lookup"><span data-stu-id="33f1c-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
