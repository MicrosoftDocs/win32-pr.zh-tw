---
description: 結束使用中的技術。
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect：： End 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322983"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="bbe5a-103">ID3DXEffect：： End 方法</span><span class="sxs-lookup"><span data-stu-id="bbe5a-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="bbe5a-104">結束使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe5a-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbe5a-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="bbe5a-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbe5a-106">Parameters</span></span>

<span data-ttu-id="bbe5a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbe5a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbe5a-108">Return value</span></span>

<span data-ttu-id="bbe5a-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbe5a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbe5a-110">這個方法一律會傳回值 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe5a-111">備註</span><span class="sxs-lookup"><span data-stu-id="bbe5a-111">Remarks</span></span>

<span data-ttu-id="bbe5a-112">效果中的所有轉譯都是在成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 **ID3DXEffect：： End** 呼叫中完成。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="bbe5a-113">轉譯所有傳遞之後，必須呼叫 **ID3DXEffect：： end** 以結束使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="bbe5a-114">效果系統會使用在呼叫 **ID3DXEffect：： begin** 時建立的狀態欄塊來回應，以在 **ID3DXEffect：： begin** 之前自動還原管線狀態。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="bbe5a-115">根據預設，效果系統會負責儲存技術之前的狀態，並在技術之後還原狀態。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="bbe5a-116">如果您選擇停用此儲存和還原功能，請參閱 [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="bbe5a-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe5a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbe5a-117">Requirements</span></span>



| <span data-ttu-id="bbe5a-118">需求</span><span class="sxs-lookup"><span data-stu-id="bbe5a-118">Requirement</span></span> | <span data-ttu-id="bbe5a-119">值</span><span class="sxs-lookup"><span data-stu-id="bbe5a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe5a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bbe5a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bbe5a-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe5a-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bbe5a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="bbe5a-122">Library</span></span><br/> | <dl> <span data-ttu-id="bbe5a-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbe5a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bbe5a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbe5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe5a-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="bbe5a-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




