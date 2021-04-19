---
description: 取得效果描述。
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect：： GetDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986772"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="780c2-103">ID3DXBaseEffect：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="780c2-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="780c2-104">取得效果描述。</span><span class="sxs-lookup"><span data-stu-id="780c2-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="780c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="780c2-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="780c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="780c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780c2-107">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="780c2-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="780c2-108">類型： **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="780c2-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="780c2-109">傳回效果的描述。</span><span class="sxs-lookup"><span data-stu-id="780c2-109">Returns a description of the effect.</span></span> <span data-ttu-id="780c2-110">請參閱 [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="780c2-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780c2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="780c2-111">Return value</span></span>

<span data-ttu-id="780c2-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="780c2-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="780c2-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="780c2-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="780c2-114">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="780c2-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="780c2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="780c2-115">Requirements</span></span>



| <span data-ttu-id="780c2-116">需求</span><span class="sxs-lookup"><span data-stu-id="780c2-116">Requirement</span></span> | <span data-ttu-id="780c2-117">值</span><span class="sxs-lookup"><span data-stu-id="780c2-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="780c2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="780c2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="780c2-119"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="780c2-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="780c2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="780c2-120">Library</span></span><br/> | <dl> <span data-ttu-id="780c2-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="780c2-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="780c2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="780c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780c2-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="780c2-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




