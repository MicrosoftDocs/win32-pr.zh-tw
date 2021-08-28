---
title: 藍牙回檔
description: 本節中的藍牙回呼函數會與可管理藍牙裝置和服務的函式搭配使用。
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588358"
---
# <a name="bluetooth-callbacks"></a>藍牙回檔

本節中的藍牙回呼函數會與可管理藍牙裝置和服務的函式搭配使用。

使用 Windows 通訊端程式設計介面也支援藍牙。 如需使用 Windows 通訊端介面進行程式設計藍牙的詳細資訊，請參閱[藍牙 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。



| 區段                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFN \_ AUTHENTICATION \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | 搭配 [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) 函式使用。                                                  |
| [**PFN \_ AUTHENTICATION \_ 回呼， \_ 例如**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | 搭配 [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) 函式使用。                                              |
| [**PFN \_ 藍牙 \_ 列舉 \_ 屬性 \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | 針對在傳遞至 [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)函式呼叫的 *pSDPStream* 參數中找到的每個屬性呼叫一次。 |
| [**PFN \_ 裝置 \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | 用於與選取藍牙裝置的關聯。                                                                                                                    |



 

 

 




