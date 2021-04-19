---
description: 發生于可用的系統事件時。
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: ITabletEventSink：： SystemEvent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992063"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="37137-103">ITabletEventSink：： SystemEvent 方法</span><span class="sxs-lookup"><span data-stu-id="37137-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="37137-104">發生于可用的系統事件時。</span><span class="sxs-lookup"><span data-stu-id="37137-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="37137-105">語法</span><span class="sxs-lookup"><span data-stu-id="37137-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="37137-106">參數</span><span class="sxs-lookup"><span data-stu-id="37137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37137-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37137-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37137-108">Tablet 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37137-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="37137-109"> \[ 中的 cid\]</span><span class="sxs-lookup"><span data-stu-id="37137-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37137-110">手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37137-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="37137-111">*活動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37137-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37137-112">系統事件代碼。</span><span class="sxs-lookup"><span data-stu-id="37137-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="37137-113">*eventdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37137-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37137-114">系統事件資料。</span><span class="sxs-lookup"><span data-stu-id="37137-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37137-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="37137-115">Return value</span></span>

<span data-ttu-id="37137-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="37137-116">This method can return one of these values.</span></span>



| <span data-ttu-id="37137-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="37137-117">Return code</span></span>                                                                            | <span data-ttu-id="37137-118">Description</span><span class="sxs-lookup"><span data-stu-id="37137-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="37137-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="37137-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="37137-120">成功。</span><span class="sxs-lookup"><span data-stu-id="37137-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="37137-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="37137-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="37137-122">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="37137-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37137-123">備註</span><span class="sxs-lookup"><span data-stu-id="37137-123">Remarks</span></span>

<span data-ttu-id="37137-124">下列清單包含事件參數的有效值。</span><span class="sxs-lookup"><span data-stu-id="37137-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="37137-125">SE \_ 點一下</span><span class="sxs-lookup"><span data-stu-id="37137-125">SE\_TAP</span></span>
-   <span data-ttu-id="37137-126">SE \_ 按兩下 \_</span><span class="sxs-lookup"><span data-stu-id="37137-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="37137-127">以 \_ 滑鼠右鍵 \_ 按一下</span><span class="sxs-lookup"><span data-stu-id="37137-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="37137-128">SE \_ 拖曳</span><span class="sxs-lookup"><span data-stu-id="37137-128">SE\_DRAG</span></span>
-   <span data-ttu-id="37137-129">SE \_ 向右 \_ 拖曳</span><span class="sxs-lookup"><span data-stu-id="37137-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="37137-130">SE \_ 按住 \_ ENTER</span><span class="sxs-lookup"><span data-stu-id="37137-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="37137-131">SE \_ 保留 \_</span><span class="sxs-lookup"><span data-stu-id="37137-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="37137-132">SE \_ 停留 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="37137-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="37137-133">SE \_ 停留 \_ 離開</span><span class="sxs-lookup"><span data-stu-id="37137-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="37137-134">SE \_ 中間 \_ 點按一下</span><span class="sxs-lookup"><span data-stu-id="37137-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="37137-135">SE \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="37137-135">SE\_KEY</span></span>
-   <span data-ttu-id="37137-136">SE \_ 輔助 \_ 按鍵</span><span class="sxs-lookup"><span data-stu-id="37137-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="37137-137">SE \_ 手勢 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="37137-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="37137-138">SE 資料 \_ 指標</span><span class="sxs-lookup"><span data-stu-id="37137-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="37137-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="37137-139">Requirements</span></span>



| <span data-ttu-id="37137-140">需求</span><span class="sxs-lookup"><span data-stu-id="37137-140">Requirement</span></span> | <span data-ttu-id="37137-141">值</span><span class="sxs-lookup"><span data-stu-id="37137-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37137-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37137-142">Minimum supported client</span></span><br/> | <span data-ttu-id="37137-143">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37137-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="37137-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37137-144">Minimum supported server</span></span><br/> | <span data-ttu-id="37137-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="37137-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="37137-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="37137-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="37137-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37137-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37137-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37137-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37137-149">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="37137-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




