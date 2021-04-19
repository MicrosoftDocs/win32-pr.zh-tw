---
description: 將網格繪製到動畫，並以指定的數量前進全域動畫時間。
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController：： AdvanceTime 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988215"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="13f54-103">ID3DXAnimationController：： AdvanceTime 方法</span><span class="sxs-lookup"><span data-stu-id="13f54-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="13f54-104">將網格繪製到動畫，並以指定的數量前進全域動畫時間。</span><span class="sxs-lookup"><span data-stu-id="13f54-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f54-105">語法</span><span class="sxs-lookup"><span data-stu-id="13f54-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="13f54-106">參數</span><span class="sxs-lookup"><span data-stu-id="13f54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f54-107">*TimeDelta* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13f54-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f54-108">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13f54-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13f54-109">前進全域動畫時間的金額（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="13f54-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="13f54-110">TimeDelta 值不能為負數或零。</span><span class="sxs-lookup"><span data-stu-id="13f54-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="13f54-111">*pCallbackHandler* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13f54-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f54-112">類型： **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="13f54-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="13f54-113">使用者定義動畫回呼處理常式介面的指標， [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md)。</span><span class="sxs-lookup"><span data-stu-id="13f54-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f54-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="13f54-114">Return value</span></span>

<span data-ttu-id="13f54-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13f54-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13f54-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="13f54-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="13f54-117">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="13f54-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f54-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="13f54-118">Requirements</span></span>



| <span data-ttu-id="13f54-119">需求</span><span class="sxs-lookup"><span data-stu-id="13f54-119">Requirement</span></span> | <span data-ttu-id="13f54-120">值</span><span class="sxs-lookup"><span data-stu-id="13f54-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13f54-121">標頭</span><span class="sxs-lookup"><span data-stu-id="13f54-121">Header</span></span><br/>  | <dl> <span data-ttu-id="13f54-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="13f54-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="13f54-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="13f54-123">Library</span></span><br/> | <dl> <span data-ttu-id="13f54-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13f54-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13f54-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f54-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="13f54-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
