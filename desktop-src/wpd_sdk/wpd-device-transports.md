---
description: WPD \_ 裝置 \_ 傳輸列舉型別會指定服務的繼承關聯性。 此列舉是由 WPD \_ 裝置 \_ 傳輸屬性所使用。
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: 'WPD_DEVICE_TRANSPORTS 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985734"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="d37a6-104">WPD \_ 裝置 \_ 傳輸列舉</span><span class="sxs-lookup"><span data-stu-id="d37a6-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="d37a6-105">[**WPD \_ 裝置 \_ 傳輸**](/windows/desktop/wpd_sdk/wpd-device-transports)列舉型別會指定服務的繼承關聯性。</span><span class="sxs-lookup"><span data-stu-id="d37a6-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="d37a6-106">此列舉是由 **WPD \_ 裝置 \_ 傳輸** 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="d37a6-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d37a6-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="d37a6-108">常數</span><span class="sxs-lookup"><span data-stu-id="d37a6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d37a6-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_ \_ 未指定 WPD 裝置傳輸 \_**</span><span class="sxs-lookup"><span data-stu-id="d37a6-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="d37a6-110">未指定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="d37a6-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="d37a6-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ 裝置 \_ 傳輸 \_ USB**</span><span class="sxs-lookup"><span data-stu-id="d37a6-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="d37a6-112">裝置透過 USB 連接。</span><span class="sxs-lookup"><span data-stu-id="d37a6-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="d37a6-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD \_ 裝置 \_ 傳輸 \_ IP**</span><span class="sxs-lookup"><span data-stu-id="d37a6-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="d37a6-114">裝置會透過網際網路通訊協定 (IP) 進行連線。</span><span class="sxs-lookup"><span data-stu-id="d37a6-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="d37a6-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD \_ 裝置 \_ 傳輸 \_ 藍牙**</span><span class="sxs-lookup"><span data-stu-id="d37a6-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="d37a6-116">裝置透過藍牙連線。</span><span class="sxs-lookup"><span data-stu-id="d37a6-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d37a6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d37a6-117">Requirements</span></span>



| <span data-ttu-id="d37a6-118">需求</span><span class="sxs-lookup"><span data-stu-id="d37a6-118">Requirement</span></span> | <span data-ttu-id="d37a6-119">值</span><span class="sxs-lookup"><span data-stu-id="d37a6-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d37a6-120">Header</span></span><br/> | <dl> <span data-ttu-id="d37a6-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="d37a6-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

