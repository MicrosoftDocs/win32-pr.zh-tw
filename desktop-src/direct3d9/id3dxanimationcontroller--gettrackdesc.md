---
description: 取得追蹤描述。
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'ID3DXAnimationController：： GetTrackDesc 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696715"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="35089-103">ID3DXAnimationController：： GetTrackDesc 方法</span><span class="sxs-lookup"><span data-stu-id="35089-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="35089-104">取得追蹤描述。</span><span class="sxs-lookup"><span data-stu-id="35089-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="35089-105">語法</span><span class="sxs-lookup"><span data-stu-id="35089-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="35089-106">參數</span><span class="sxs-lookup"><span data-stu-id="35089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35089-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35089-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35089-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35089-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35089-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="35089-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="35089-110">*pDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="35089-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35089-111">類型： **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="35089-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="35089-112">追蹤描述的指標。</span><span class="sxs-lookup"><span data-stu-id="35089-112">Pointer to the track description.</span></span> <span data-ttu-id="35089-113">請參閱 [**D3DXTRACK \_ DESC**](d3dxtrack-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="35089-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35089-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="35089-114">Return value</span></span>

<span data-ttu-id="35089-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35089-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35089-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="35089-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="35089-117">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="35089-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="35089-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="35089-118">Requirements</span></span>



| <span data-ttu-id="35089-119">需求</span><span class="sxs-lookup"><span data-stu-id="35089-119">Requirement</span></span> | <span data-ttu-id="35089-120">值</span><span class="sxs-lookup"><span data-stu-id="35089-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35089-121">標頭</span><span class="sxs-lookup"><span data-stu-id="35089-121">Header</span></span><br/>  | <dl> <span data-ttu-id="35089-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="35089-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="35089-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="35089-123">Library</span></span><br/> | <dl> <span data-ttu-id="35089-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35089-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35089-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35089-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35089-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="35089-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
