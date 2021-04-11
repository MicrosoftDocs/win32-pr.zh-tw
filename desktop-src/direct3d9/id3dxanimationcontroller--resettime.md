---
description: 將全域動畫的時間重設為零。 任何暫止的事件將會保留其原始排程，但在新的時間範圍內。
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController：： ResetTime 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696751"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="0efd0-104">ID3DXAnimationController：： ResetTime 方法</span><span class="sxs-lookup"><span data-stu-id="0efd0-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="0efd0-105">將全域動畫的時間重設為零。</span><span class="sxs-lookup"><span data-stu-id="0efd0-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="0efd0-106">任何暫止的事件將會保留其原始排程，但在新的時間範圍內。</span><span class="sxs-lookup"><span data-stu-id="0efd0-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efd0-107">語法</span><span class="sxs-lookup"><span data-stu-id="0efd0-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="0efd0-108">參數</span><span class="sxs-lookup"><span data-stu-id="0efd0-108">Parameters</span></span>

<span data-ttu-id="0efd0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0efd0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0efd0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0efd0-110">Return value</span></span>

<span data-ttu-id="0efd0-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0efd0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0efd0-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0efd0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0efd0-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0efd0-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efd0-114">備註</span><span class="sxs-lookup"><span data-stu-id="0efd0-114">Remarks</span></span>

<span data-ttu-id="0efd0-115">當全域動畫時間值接近 DOUBLE 儲存體的最大有效位數，或2⁶⁴-1 時，通常會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="0efd0-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0efd0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0efd0-116">Requirements</span></span>



| <span data-ttu-id="0efd0-117">需求</span><span class="sxs-lookup"><span data-stu-id="0efd0-117">Requirement</span></span> | <span data-ttu-id="0efd0-118">值</span><span class="sxs-lookup"><span data-stu-id="0efd0-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0efd0-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0efd0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0efd0-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="0efd0-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0efd0-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="0efd0-121">Library</span></span><br/> | <dl> <span data-ttu-id="0efd0-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0efd0-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0efd0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0efd0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efd0-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0efd0-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




