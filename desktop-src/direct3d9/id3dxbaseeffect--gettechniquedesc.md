---
description: 取得技術描述。
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect：： GetTechniqueDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196437"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="87b21-103">ID3DXBaseEffect：： GetTechniqueDesc 方法</span><span class="sxs-lookup"><span data-stu-id="87b21-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="87b21-104">取得技術描述。</span><span class="sxs-lookup"><span data-stu-id="87b21-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b21-105">語法</span><span class="sxs-lookup"><span data-stu-id="87b21-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="87b21-106">參數</span><span class="sxs-lookup"><span data-stu-id="87b21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b21-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87b21-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b21-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="87b21-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="87b21-109">技術控點。</span><span class="sxs-lookup"><span data-stu-id="87b21-109">Technique handle.</span></span> <span data-ttu-id="87b21-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="87b21-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="87b21-111">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="87b21-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87b21-112">類型： **[ **D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="87b21-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="87b21-113">傳回技術的描述。</span><span class="sxs-lookup"><span data-stu-id="87b21-113">Returns a description of the technique.</span></span> <span data-ttu-id="87b21-114">請參閱 [**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="87b21-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b21-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="87b21-115">Return value</span></span>

<span data-ttu-id="87b21-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87b21-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87b21-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="87b21-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="87b21-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="87b21-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="87b21-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="87b21-119">Requirements</span></span>



| <span data-ttu-id="87b21-120">需求</span><span class="sxs-lookup"><span data-stu-id="87b21-120">Requirement</span></span> | <span data-ttu-id="87b21-121">值</span><span class="sxs-lookup"><span data-stu-id="87b21-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b21-122">標頭</span><span class="sxs-lookup"><span data-stu-id="87b21-122">Header</span></span><br/>  | <dl> <span data-ttu-id="87b21-123"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="87b21-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="87b21-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="87b21-124">Library</span></span><br/> | <dl> <span data-ttu-id="87b21-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87b21-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="87b21-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87b21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b21-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="87b21-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




