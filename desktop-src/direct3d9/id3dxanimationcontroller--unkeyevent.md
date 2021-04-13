---
description: 從動畫播放軌移除指定的事件，以防止事件的執行。
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'ID3DXAnimationController：： UnkeyEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323355"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="62e33-103">ID3DXAnimationController：： UnkeyEvent 方法</span><span class="sxs-lookup"><span data-stu-id="62e33-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="62e33-104">從動畫播放軌移除指定的事件，以防止事件的執行。</span><span class="sxs-lookup"><span data-stu-id="62e33-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e33-105">語法</span><span class="sxs-lookup"><span data-stu-id="62e33-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="62e33-106">參數</span><span class="sxs-lookup"><span data-stu-id="62e33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e33-107">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62e33-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e33-108">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="62e33-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="62e33-109">要從動畫播放軌移除之事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="62e33-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e33-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="62e33-110">Return value</span></span>

<span data-ttu-id="62e33-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62e33-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62e33-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="62e33-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="62e33-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="62e33-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e33-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="62e33-114">Requirements</span></span>



| <span data-ttu-id="62e33-115">需求</span><span class="sxs-lookup"><span data-stu-id="62e33-115">Requirement</span></span> | <span data-ttu-id="62e33-116">值</span><span class="sxs-lookup"><span data-stu-id="62e33-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62e33-117">標頭</span><span class="sxs-lookup"><span data-stu-id="62e33-117">Header</span></span><br/>  | <dl> <span data-ttu-id="62e33-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="62e33-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="62e33-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="62e33-119">Library</span></span><br/> | <dl> <span data-ttu-id="62e33-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62e33-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62e33-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62e33-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e33-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="62e33-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




