---
description: 定義傳遞至 WFD \_ 顯示 \_ 接收 \_ 通知回呼函式的通知類型 \_ 。
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: 'WFD_DISPLAY_SINK_NOTIFICATION_TYPE 列舉 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971780"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="88060-103">WFD \_ 顯示 \_ 接收 \_ 通知 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="88060-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="88060-104">[ **Wfd \_ 顯示 \_ 接收 \_ 通知 \_ 類型** ] 列舉類型會定義傳遞至 [ [**wfd \_ 顯示 \_ 接收] \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式的通知類型。</span><span class="sxs-lookup"><span data-stu-id="88060-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="88060-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88060-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="88060-106">常數</span><span class="sxs-lookup"><span data-stu-id="88060-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88060-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="88060-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="88060-108">通知是布建要求。</span><span class="sxs-lookup"><span data-stu-id="88060-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="88060-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="88060-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="88060-110">通知是重新連接要求。</span><span class="sxs-lookup"><span data-stu-id="88060-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="88060-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="88060-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="88060-112">通知是已連線的通知。</span><span class="sxs-lookup"><span data-stu-id="88060-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="88060-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="88060-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="88060-114">通知是已中斷連線的通知。</span><span class="sxs-lookup"><span data-stu-id="88060-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88060-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="88060-115">Requirements</span></span>



| <span data-ttu-id="88060-116">需求</span><span class="sxs-lookup"><span data-stu-id="88060-116">Requirement</span></span> | <span data-ttu-id="88060-117">值</span><span class="sxs-lookup"><span data-stu-id="88060-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="88060-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88060-118">Minimum supported client</span></span><br/> | <span data-ttu-id="88060-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88060-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="88060-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88060-120">Minimum supported server</span></span><br/> | <span data-ttu-id="88060-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88060-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="88060-122">標頭</span><span class="sxs-lookup"><span data-stu-id="88060-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="88060-123"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="88060-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




