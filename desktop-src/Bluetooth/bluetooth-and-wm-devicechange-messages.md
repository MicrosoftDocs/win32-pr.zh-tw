---
title: 藍牙和 WM_DEVICECHANGE 訊息
description: 藍牙包含特定 \_ 的 WM DEVICECHANGE 訊息，可讓開發人員在 Bluetooth 裝置變更狀態時取得訊息。
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933326"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="ef7d8-103">藍牙和 WM \_ DEVICECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="ef7d8-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="ef7d8-104">藍牙包含特定的 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息，可讓開發人員在 Bluetooth 裝置變更狀態時取得訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="ef7d8-105">本主題說明如何接收藍牙特定的 **WM \_ DEVICECHANGE** 訊息，並列出藍牙特定的訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="ef7d8-106">接收藍牙特定的 WM \_ DEVICECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="ef7d8-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="ef7d8-107">若要接收 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息，必須先開啟本機無線電的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="ef7d8-108">若要執行此工作，請使用下列的其中一個方法：</span><span class="sxs-lookup"><span data-stu-id="ef7d8-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="ef7d8-109">使用 [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) 函式搭配下列參數： (GUID \_ BTHPORT \_ 裝置 \_ 介面 ...、DIGCF \_ 目前 \| DIGCF \_ DEVICEINTERFACE) ，然後使用 [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)、 [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx)、 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)和 [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) 函數。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="ef7d8-110">使用 [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)、 [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)和 [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) 函數。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="ef7d8-111">開啟藍牙無線電控點時，呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 函式，並使用 **DBT \_ DEVTYP \_ 控制碼** 作為 devicetype，在控制碼上註冊通知。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="ef7d8-112">註冊時，會傳送下列 Guid，而 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)：：**dbch \_ 資料** 成員是相關聯的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="ef7d8-113">藍牙特定訊息</span><span class="sxs-lookup"><span data-stu-id="ef7d8-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="ef7d8-114">下表列出藍牙特定的 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="ef7d8-115">GUID</span><span class="sxs-lookup"><span data-stu-id="ef7d8-115">GUID</span></span>                                   | <span data-ttu-id="ef7d8-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="ef7d8-116">BUFFER</span></span>                                                  | <span data-ttu-id="ef7d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="ef7d8-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7d8-118">GUID \_ 藍牙 \_ HCI \_ 事件</span><span class="sxs-lookup"><span data-stu-id="ef7d8-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="ef7d8-119">**BTH \_ HCI \_ 事件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="ef7d8-120">當遠端 Bluetooth 裝置在 ACL 層級連線或中斷連線時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ef7d8-121">GUID \_ 藍牙 \_ L2CAP \_ 事件</span><span class="sxs-lookup"><span data-stu-id="ef7d8-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="ef7d8-122">**BTH \_ L2CAP \_ 事件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="ef7d8-123">當本機無線電裝置與遠端 Bluetooth 裝置之間的 L2CAP 通道已建立或終止時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="ef7d8-124">針對 multiplexers 的 L2CAP 通道（例如 RFCOMM），只會在建立基礎通道時傳送此訊息，而不會在每個多工通道（例如 RFCOMM 通道）建立或終止時傳送。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="ef7d8-125">GUID \_ 藍牙 \_ PIN \_ 要求</span><span class="sxs-lookup"><span data-stu-id="ef7d8-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="ef7d8-126">不適用。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-126">Not applicable.</span></span>                                         | <span data-ttu-id="ef7d8-127">應用程式應該忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-127">This message should be ignored by the application.</span></span> <span data-ttu-id="ef7d8-128">如果應用程式必須接收 PIN 要求，則應該使用 [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) 函式。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="ef7d8-129">\_ \_ \_ 範圍中的 GUID 藍牙無線電 \_</span><span class="sxs-lookup"><span data-stu-id="ef7d8-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="ef7d8-130">**BTH \_ \_ 範圍中的收音機 \_**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="ef7d8-131">當遠端藍牙裝置的下列任何屬性變更時，就會傳送此訊息：已探索到裝置、裝置類別、名稱、線上狀態或已記住的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="ef7d8-132">當設定或清除這些屬性時，也會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="ef7d8-133">GUID \_ 藍牙 \_ 無線電 \_ 超出 \_ \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="ef7d8-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="ef7d8-134">**藍牙 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="ef7d8-135">當最後一次查詢完成之後，找不到先前探索到的裝置時，就會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="ef7d8-136">此訊息不會傳送給記住的裝置。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="ef7d8-137">**BTH \_ 位址** 結構是找不到的裝置位址。</span><span class="sxs-lookup"><span data-stu-id="ef7d8-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ef7d8-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef7d8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef7d8-139">**BluetoothFindFirstRadio**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="ef7d8-140">**BluetoothFindNextRadio**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="ef7d8-141">**BluetoothFindRadioClose**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="ef7d8-142">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="ef7d8-143">SetupDiDestroyDeviceInfoList</span><span class="sxs-lookup"><span data-stu-id="ef7d8-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="ef7d8-144">SetupDiEnumDeviceInterfaces</span><span class="sxs-lookup"><span data-stu-id="ef7d8-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="ef7d8-145">SetupDiGetClassDevs</span><span class="sxs-lookup"><span data-stu-id="ef7d8-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="ef7d8-146">**藍牙 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="ef7d8-147">**BTH \_ HCI \_ 事件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="ef7d8-148">**BTH \_ L2CAP \_ 事件 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="ef7d8-149">**BTH \_ \_ 範圍中的收音機 \_**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="ef7d8-150">**開發 \_ 廣播 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="ef7d8-151">**WM \_ DEVICECHANGE**</span><span class="sxs-lookup"><span data-stu-id="ef7d8-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 