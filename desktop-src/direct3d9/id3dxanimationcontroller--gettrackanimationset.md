---
description: 取得指定之播放軌的動畫集。
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController：： GetTrackAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946168"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="39ec1-103">ID3DXAnimationController：： GetTrackAnimationSet 方法</span><span class="sxs-lookup"><span data-stu-id="39ec1-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="39ec1-104">取得指定之播放軌的動畫集。</span><span class="sxs-lookup"><span data-stu-id="39ec1-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ec1-105">語法</span><span class="sxs-lookup"><span data-stu-id="39ec1-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="39ec1-106">參數</span><span class="sxs-lookup"><span data-stu-id="39ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ec1-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39ec1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ec1-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39ec1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39ec1-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="39ec1-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="39ec1-110">*ppAnimSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39ec1-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39ec1-111">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="39ec1-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="39ec1-112">針對給定的播放軌所設定的 [**ID3DXAnimationSet**](id3dxanimationset.md) 動畫指標。</span><span class="sxs-lookup"><span data-stu-id="39ec1-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ec1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="39ec1-113">Return value</span></span>

<span data-ttu-id="39ec1-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39ec1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39ec1-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="39ec1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="39ec1-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="39ec1-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ec1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="39ec1-117">Requirements</span></span>



| <span data-ttu-id="39ec1-118">需求</span><span class="sxs-lookup"><span data-stu-id="39ec1-118">Requirement</span></span> | <span data-ttu-id="39ec1-119">值</span><span class="sxs-lookup"><span data-stu-id="39ec1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39ec1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="39ec1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="39ec1-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="39ec1-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="39ec1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="39ec1-122">Library</span></span><br/> | <dl> <span data-ttu-id="39ec1-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="39ec1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39ec1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39ec1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ec1-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="39ec1-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
