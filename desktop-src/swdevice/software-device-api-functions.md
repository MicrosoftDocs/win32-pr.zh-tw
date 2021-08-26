---
title: 軟體裝置 API 函式
description: 本節說明用戶端應用程式所呼叫的軟體裝置 API 函式，以及用戶端應用程式所執行的回呼函數。
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f5d525eb9a4d4bc9af4807a2b3ad069b109b17874040e84cb3a9059d31bb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937088"
---
# <a name="software-device-api-functions"></a>軟體裝置 API 函式

本節說明用戶端應用程式所呼叫的軟體裝置 API 函式，以及用戶端應用程式所執行的回呼函數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                           | 描述                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | 關閉軟體裝置控制碼。 當控制碼關閉時，PnP 將會起始移除裝置的進程。<br/>                                   |
| [**SW \_ 裝置 \_ 建立 \_ 回呼**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | 提供在登錄中支援的裝置，並可讓呼叫者使用 *hSwDevice* 控制碼呼叫軟體裝置 API 函式。<br/> |
| [**SwDeviceCreate**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | 起始軟體裝置的列舉。<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | 取得軟體裝置的存留期。 <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | 設定軟體裝置介面上的屬性。 <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | 註冊軟體裝置的裝置介面，並選擇性地設定該介面上的屬性。 <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | 啟用或停用軟體裝置的裝置介面。 <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | 設定軟體裝置上的屬性。 <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | 管理軟體裝置的存留期。 <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | 釋出其他軟體裝置 API 功能所配置的記憶體。<br/>                                                                                      |



 

 

 

[將關於本主題的意見傳送給 Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")