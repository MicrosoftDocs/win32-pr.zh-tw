---
description: 描述傳遞至 WFD \_ 顯示 \_ 接收 \_ 通知回呼函式的通知 \_ 。
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: 'WFD_DISPLAY_SINK_NOTIFICATION 結構 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981558"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="c6c43-103">WFD \_ 顯示 \_ 接收 \_ 通知結構</span><span class="sxs-lookup"><span data-stu-id="c6c43-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="c6c43-104">[ **Wfd \_ 顯示 \_ 接收] \_ 通知** 結構描述傳遞至 [ [**wfd \_ 顯示接收] \_ \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式的通知。</span><span class="sxs-lookup"><span data-stu-id="c6c43-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c43-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6c43-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="c6c43-106">成員</span><span class="sxs-lookup"><span data-stu-id="c6c43-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6c43-107">**標頭**</span><span class="sxs-lookup"><span data-stu-id="c6c43-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-108">可描述通知中所含資料的 [**WFD \_ 顯示 \_ 接收器 \_ 物件 \_ 標頭**](wfd-display-sink-object-header.md) 。</span><span class="sxs-lookup"><span data-stu-id="c6c43-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-109">**type**</span><span class="sxs-lookup"><span data-stu-id="c6c43-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-110">指出通知類型的 [ [**WFD \_ 顯示 \_ 接收] \_ 通知 \_ 類型**](wfd-display-sink-notification-type.md) 值。</span><span class="sxs-lookup"><span data-stu-id="c6c43-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="c6c43-111">此參數也會決定要在下聯集內使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="c6c43-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-112">**strRemoteDeviceName**</span><span class="sxs-lookup"><span data-stu-id="c6c43-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-113">包含以 Null 終止的字串，其中包含遠端裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6c43-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="c6c43-114">[WFD \_ 接收器 \_ 最大 \_ 裝置 \_ 名稱長度] \_ 定義為 (32) 的值。</span><span class="sxs-lookup"><span data-stu-id="c6c43-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-115">**RemoteDeviceAddress**</span><span class="sxs-lookup"><span data-stu-id="c6c43-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-116">[**DOT11 \_ MAC \_ 位址**](dot11-mac-address-type.md)，其中包含遠端裝置的 BSSID。</span><span class="sxs-lookup"><span data-stu-id="c6c43-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-117">**ProvisioningRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="c6c43-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-118">布建要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6c43-118">Info about a provisioning request.</span></span> <span data-ttu-id="c6c43-119">如果 *類型* 具有值 **ProvisioningRequestNotification**，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="c6c43-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="c6c43-120">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="c6c43-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-121">會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6c43-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-122">**PossibleConfigMethods**</span><span class="sxs-lookup"><span data-stu-id="c6c43-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-123">顯示 UI 以進行互動式接受的可能方法。</span><span class="sxs-lookup"><span data-stu-id="c6c43-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c6c43-124">**ReconnectRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="c6c43-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-125">重新連接要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6c43-125">Info about a reconnect request.</span></span> <span data-ttu-id="c6c43-126">如果 *類型* 具有值 **ReconnectRequestNotification**，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="c6c43-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="c6c43-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="c6c43-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-128">群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6c43-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c6c43-129">**ConnectedInfo**</span><span class="sxs-lookup"><span data-stu-id="c6c43-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-130">連線通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6c43-130">Info about a connected notification.</span></span> <span data-ttu-id="c6c43-131">如果 *類型* 具有值 **ConnectedNotification**，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="c6c43-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="c6c43-132">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="c6c43-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-133">會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6c43-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-134">**guidSessionInterface**</span><span class="sxs-lookup"><span data-stu-id="c6c43-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-135">指出會話介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c6c43-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="c6c43-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-137">群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6c43-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-138">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="c6c43-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-139">描述設定檔之以 Null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="c6c43-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="c6c43-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-141">本機位址。</span><span class="sxs-lookup"><span data-stu-id="c6c43-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="c6c43-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-143">遠端位址。</span><span class="sxs-lookup"><span data-stu-id="c6c43-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="c6c43-144">**uRTSPPort**</span><span class="sxs-lookup"><span data-stu-id="c6c43-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="c6c43-145">RTSP 埠。</span><span class="sxs-lookup"><span data-stu-id="c6c43-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6c43-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c43-146">Requirements</span></span>



| <span data-ttu-id="c6c43-147">需求</span><span class="sxs-lookup"><span data-stu-id="c6c43-147">Requirement</span></span> | <span data-ttu-id="c6c43-148">值</span><span class="sxs-lookup"><span data-stu-id="c6c43-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c43-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c43-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c43-150">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c43-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6c43-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c43-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c43-152">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c43-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6c43-153">標頭</span><span class="sxs-lookup"><span data-stu-id="c6c43-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c43-154"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c43-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




