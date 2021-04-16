---
description: 執行必要的初始化，以允許呼叫的應用程式成為 Miracast 顯示接收。
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: 'WFDDisplaySinkStart 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512765"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="f31bc-103">WFDDisplaySinkStart 函式</span><span class="sxs-lookup"><span data-stu-id="f31bc-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="f31bc-104">執行必要的初始化，以允許呼叫的應用程式成為 Miracast 顯示接收。</span><span class="sxs-lookup"><span data-stu-id="f31bc-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="f31bc-105">您的應用程式應該在啟動時呼叫此一次。</span><span class="sxs-lookup"><span data-stu-id="f31bc-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31bc-106">語法</span><span class="sxs-lookup"><span data-stu-id="f31bc-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="f31bc-107">參數</span><span class="sxs-lookup"><span data-stu-id="f31bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31bc-108">*uDeviceCategory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31bc-109">裝置類別。</span><span class="sxs-lookup"><span data-stu-id="f31bc-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="f31bc-110">*uSubCategory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31bc-111">裝置子類別。</span><span class="sxs-lookup"><span data-stu-id="f31bc-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="f31bc-112">*pCallbackCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f31bc-113">選用的內容指標，會傳遞給 *pfnCallback* 參數中指定的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f31bc-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f31bc-114">*pfnCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31bc-115">只要有應用程式的通知，就會呼叫回呼函式的指標。</span><span class="sxs-lookup"><span data-stu-id="f31bc-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="f31bc-116">可傳送的通知會在 [ [**WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼**](wfd-display-sink-notification-callback.md)] 中描述。</span><span class="sxs-lookup"><span data-stu-id="f31bc-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31bc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f31bc-117">Return value</span></span>

<span data-ttu-id="f31bc-118">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="f31bc-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f31bc-119">如果函式失敗，則傳回值可能是下列其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="f31bc-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="f31bc-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f31bc-120">Return code</span></span>                                                                                          | <span data-ttu-id="f31bc-121">Description</span><span class="sxs-lookup"><span data-stu-id="f31bc-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="f31bc-122"><dt>**\_不 \_ 支援的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="f31bc-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="f31bc-123">此硬體不支援顯示接收。</span><span class="sxs-lookup"><span data-stu-id="f31bc-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f31bc-124">備註</span><span class="sxs-lookup"><span data-stu-id="f31bc-124">Remarks</span></span>

<span data-ttu-id="f31bc-125">此函式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="f31bc-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="f31bc-126">讓電腦可供探索</span><span class="sxs-lookup"><span data-stu-id="f31bc-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="f31bc-127">設定 P2P 裝置資訊以反映指定的類別和子類別</span><span class="sxs-lookup"><span data-stu-id="f31bc-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="f31bc-128">將所有 Wi-Fi 直接畫面上的 Miracast 設定為接收的裝置類型</span><span class="sxs-lookup"><span data-stu-id="f31bc-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="f31bc-129">註冊要在有連入連線時叫用的指定回呼</span><span class="sxs-lookup"><span data-stu-id="f31bc-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="f31bc-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f31bc-130">Requirements</span></span>



| <span data-ttu-id="f31bc-131">需求</span><span class="sxs-lookup"><span data-stu-id="f31bc-131">Requirement</span></span> | <span data-ttu-id="f31bc-132">值</span><span class="sxs-lookup"><span data-stu-id="f31bc-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31bc-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f31bc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f31bc-134">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f31bc-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f31bc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f31bc-136">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f31bc-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f31bc-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f31bc-137">End of client support</span></span><br/>    | <span data-ttu-id="f31bc-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f31bc-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="f31bc-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f31bc-139">End of server support</span></span><br/>    | <span data-ttu-id="f31bc-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f31bc-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="f31bc-141">標頭</span><span class="sxs-lookup"><span data-stu-id="f31bc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f31bc-142"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="f31bc-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="f31bc-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="f31bc-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f31bc-144"><dt>Wifidisplay .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f31bc-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="f31bc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f31bc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f31bc-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31bc-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31bc-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f31bc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31bc-148">**WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="f31bc-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




