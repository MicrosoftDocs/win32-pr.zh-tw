---
title: IMsTscAxEvents OnFocusReleased 方法
description: 在按下放開焦點按鍵組合時呼叫。 例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- OnFocusReleased 方法遠端桌面服務
- OnFocusReleased 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnFocusReleased 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965731"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="bc279-107">IMsTscAxEvents：： OnFocusReleased 方法</span><span class="sxs-lookup"><span data-stu-id="bc279-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="bc279-108">在按下放開焦點按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc279-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="bc279-109">例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="bc279-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="bc279-110">此事件可讓 ActiveX 控制項容器離開 ActiveX 控制項的控制權。</span><span class="sxs-lookup"><span data-stu-id="bc279-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="bc279-111">例如，這在您沒有滑鼠的情況下很有用，而像 ALT + TAB 等特殊按鍵組合會重新導向至伺服器。</span><span class="sxs-lookup"><span data-stu-id="bc279-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="bc279-112">在此情況下，您沒有辦法將鍵盤焦點傳回本機桌面。</span><span class="sxs-lookup"><span data-stu-id="bc279-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="bc279-113">不過，使用 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵組合時，ActiveX 容器可以接聽此事件，並將焦點從 ActiveX 控制項移出以回應。</span><span class="sxs-lookup"><span data-stu-id="bc279-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc279-114">語法</span><span class="sxs-lookup"><span data-stu-id="bc279-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="bc279-115">參數</span><span class="sxs-lookup"><span data-stu-id="bc279-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc279-116">*iDirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc279-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc279-117">1 (CTRL + ALT + 向右鍵的方向參數) 或 1 (CTRL + ALT + 向左鍵) 。</span><span class="sxs-lookup"><span data-stu-id="bc279-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc279-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc279-118">Return value</span></span>

<span data-ttu-id="bc279-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bc279-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc279-120">備註</span><span class="sxs-lookup"><span data-stu-id="bc279-120">Remarks</span></span>

<span data-ttu-id="bc279-121">當用戶端上使用遠端桌面連線6.0 時，就可以使用此事件。</span><span class="sxs-lookup"><span data-stu-id="bc279-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc279-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc279-122">Requirements</span></span>



| <span data-ttu-id="bc279-123">需求</span><span class="sxs-lookup"><span data-stu-id="bc279-123">Requirement</span></span> | <span data-ttu-id="bc279-124">值</span><span class="sxs-lookup"><span data-stu-id="bc279-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc279-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc279-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc279-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc279-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bc279-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc279-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc279-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc279-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bc279-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bc279-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc279-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc279-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc279-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bc279-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc279-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc279-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc279-133">IID</span><span class="sxs-lookup"><span data-stu-id="bc279-133">IID</span></span><br/>                      | <span data-ttu-id="bc279-134">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bc279-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bc279-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc279-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc279-136">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bc279-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





