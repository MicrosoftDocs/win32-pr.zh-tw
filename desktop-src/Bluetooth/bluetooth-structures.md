---
title: 藍牙結構
description: 本節提供用來管理藍牙裝置和服務之結構的定義。
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- 藍牙、參考、結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588278"
---
# <a name="bluetooth-structures"></a>藍牙結構

本節提供用來管理藍牙裝置和服務之結構的定義。

使用 Windows 通訊端程式設計介面也支援藍牙。 如需使用 Windows 通訊端介面進行程式設計藍牙的詳細資訊，請參閱[藍牙 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。



| 區段                                                                                       | Content                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**藍牙 \_ 位址**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | 包含藍牙裝置的位址。                                                                                      |
| [**藍牙 \_ 驗證 \_ 回呼 \_ 參數**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | 包含回應驗證要求之藍牙裝置的特定設定資訊。                  |
| [**藍牙 \_ 驗證 \_ 回應**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | 包含為了回應 BTH \_ 遠端 \_ 驗證要求事件而傳遞的資訊 \_ 。                                           |
| [**藍牙 \_ 貨 \_ 組**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | 提供裝置藍牙類別的規格和抓取 () 的資訊。                                         |
| [**藍牙 \_ 裝置 \_ 資訊**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | 提供藍牙裝置的相關資訊。                                                                                   |
| [**藍牙 \_ 裝置 \_ 搜尋 \_ 參數**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | 指定藍牙裝置搜尋的搜尋準則。                                                                         |
| [**藍牙 \_ 尋找 \_ 單選 \_ 參數**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | 有助於列舉已安裝的藍牙無線電。                                                                       |
| [**藍牙 \_ 本地 \_ 服務 \_ 資訊**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | 包含藍牙電臺的本機服務資訊。                                                                        |
| [**藍牙 \_ 數值 \_ 比較 \_ 資訊**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | 包含用來透過數值比較進行驗證的數值。                                                       |
| [**藍牙 \_ OOB \_ 資料 \_ 資訊**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | 包含用來在建立頻外裝置配對之前進行驗證的資料。                                          |
| [**藍牙通行 \_ 金鑰 \_ 資訊**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | 包含用來透過密碼驗證的密碼。                                                                        |
| [**藍牙 \_ PIN \_ 資訊**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | 包含用來透過 PIN 進行驗證的資訊。                                                                            |
| [**藍牙 \_ 無線電 \_ 資訊**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | 包含藍牙電臺的相關資訊。                                                                                    |
| [**藍牙 \_ 選取 \_ 裝置 \_ 參數**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | 協助並管理藍牙裝置和服務的可見度、驗證和選取。                         |
| [**BTH \_ 裝置 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | 儲存藍牙裝置的相關資訊。                                                                                     |
| [**BTH \_ HCI \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | 用於與取得藍牙之 WM \_ DEVICECHANGE 訊息的連接。                                                       |
| [**BTH \_ L2CAP \_ 事件 \_ 資訊**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | 包含與 L2CAP 通道相關聯之事件的相關資料。                                                        |
| [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | 用於查詢藍牙裝置是否存在。                                                                       |
| [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | 用來查詢藍牙服務。                                                                                               |
| [**BTH \_ \_ 範圍中的收音機 \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | 儲存位於通訊範圍內藍牙裝置的相關資料。                                                     |
| [**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | 提供指定藍牙服務的服務資訊。                                                                |
| [**SDP \_ 元素 \_ 資料**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | 儲存 SDP 元素資料。                                                                                                         |
| [**SDP \_ 字串 \_ 類型 \_ 資料**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | 儲存有關 SDP 字串類型的資訊。                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | 用於藍牙查詢中，以限制要在查詢中傳回的屬性集。                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | 協助搜尋 Uuid。                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | 包含要在其上執行 SDP 查詢的 UUID。 搭配 [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) 結構使用。 |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | 與 AF BTH 位址系列所定義的藍牙通訊端作業搭配使用 \_ 。                                   |



 

 

 




