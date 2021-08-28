---
title: 藍牙和 WM_DEVICECHANGE 訊息
description: 藍牙包含特定 \_ 的 WM DEVICECHANGE 訊息，可讓開發人員在藍牙裝置發生狀態變更時取得訊息。
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b22c08c4243ce33f7d3146e96a3fcdd5c937b4781fd783918c148939ca0e22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588408"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>藍牙和 WM \_ DEVICECHANGE 訊息

藍牙包含特定的 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)訊息，可讓開發人員在藍牙裝置發生狀態變更時取得訊息。 本主題說明如何接收藍牙特定的 **WM \_ DEVICECHANGE** 訊息，並列出藍牙特定的訊息。

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>接收藍牙特定的 WM \_ DEVICECHANGE 訊息

若要接收 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息，必須先開啟本機無線電的控制碼。 若要執行此工作，請使用下列的其中一個方法：

-   使用 [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) 函式搭配下列參數： (GUID \_ BTHPORT \_ 裝置 \_ 介面 ...、DIGCF \_ 目前 \| DIGCF \_ DEVICEINTERFACE) ，然後使用 [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)、 [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx)、 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)和 [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) 函數。
-   使用 [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)、 [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)和 [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) 函數。

當藍牙的無線電控制碼開啟時，呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)函式，並使用 **DBT \_ DEVTYP \_ 控制碼** 作為 devicetype，在控制碼上註冊通知。 註冊時，會傳送下列 Guid，而 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)：：**dbch \_ 資料** 成員是相關聯的緩衝區。

## <a name="bluetooth-specific-messages"></a>藍牙特定的訊息

下表列出藍牙特定的 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)訊息。

| GUID                                   | BUFFER                                                  | 描述                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ 藍牙 \_ HCI \_ 事件            | [**BTH \_ HCI \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | 當遠端藍牙裝置在 ACL 層級連線或中斷連線時，就會傳送此訊息。                                                                                                                                                                                                                                                                    |
| GUID \_ 藍牙 \_ L2CAP \_ 事件          | [**BTH \_ L2CAP \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | 當本機無線電和遠端藍牙裝置之間的 L2CAP 通道已建立或終止時，就會傳送此訊息。 針對 multiplexers 的 L2CAP 通道（例如 RFCOMM），只會在建立基礎通道時傳送此訊息，而不會在每個多工通道（例如 RFCOMM 通道）建立或終止時傳送。 |
| GUID \_ 藍牙 \_ PIN \_ 要求          | 不適用。                                         | 應用程式應該忽略此訊息。 如果應用程式必須接收 PIN 要求，則應該使用 [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) 函式。                                                                                                                                                   |
| \_ \_ \_ 範圍中的 GUID 藍牙無線電 \_      | [**BTH \_ \_ 範圍中的收音機 \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | 當遠端藍牙裝置的下列任何屬性變更時，就會傳送此訊息：已探索到裝置、裝置類別、名稱、線上狀態或已記住的裝置狀態。 當設定或清除這些屬性時，也會傳送此訊息。                                                                                  |
| GUID \_ 藍牙 \_ 無線電 \_ 超出 \_ \_ 範圍 | [**藍牙 \_ 位址**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | 當最後一次查詢完成之後，找不到先前探索到的裝置時，就會傳送此訊息。 此訊息不會傳送給記住的裝置。 **BTH \_ 位址** 結構是找不到的裝置位址。                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**藍牙 \_ 位址**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**BTH \_ HCI \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**BTH \_ L2CAP \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ \_ 範圍中的收音機 \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 