---
title: 藍牙回呼
description: 本節中的藍牙回呼函式會與能夠管理藍牙裝置和服務的函式搭配使用。
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671608"
---
# <a name="bluetooth-callbacks"></a>藍牙回呼

本節中的藍牙回呼函式會與能夠管理藍牙裝置和服務的函式搭配使用。

您也可以使用 Windows 通訊端程式設計介面來支援藍牙。 如需使用 Windows 通訊端介面進行藍牙程式設計的詳細資訊，請參閱 [適用于藍牙的 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。



| 區段                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFN \_ AUTHENTICATION \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | 搭配 [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) 函式使用。                                                  |
| [**PFN \_ AUTHENTICATION \_ 回呼， \_ 例如**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | 搭配 [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) 函式使用。                                              |
| [**PFN \_ 藍牙 \_ 列舉 \_ 屬性 \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | 針對在傳遞至 [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)函式呼叫的 *pSDPStream* 參數中找到的每個屬性呼叫一次。 |
| [**PFN \_ 裝置 \_ 回呼**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | 用於與選取藍牙裝置的關聯。                                                                                                                    |



 

 

 




