---
description: 您可以使用 GUID 值來描述裝置介面。 Windows 可攜式裝置會定義下列裝置介面。
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: '裝置介面 Guid (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977555"
---
# <a name="device-interface-guids"></a>裝置介面 Guid

您可以使用 **GUID** 值來描述裝置介面。 Windows 可攜式裝置會定義下列裝置介面。



| 常數                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | 識別出現在一般 WPD 列舉中的裝置。 當應用程式呼叫 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) 方法時，將會列舉任何註冊此介面 GUID 的裝置。<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ 私用**</dt> </dl> | 識別不會在一般 WPD 列舉期間出現的裝置。 只有當應用程式呼叫 [**IPortableDeviceManager：： GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) 方法時，才會列舉任何註冊此介面 GUID 的裝置。<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ 服務**</dt> </dl> | 在 Windows 7 中，應用程式可以藉由呼叫 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) ，並使用此介面類別別做為服務類型 GUID，來列舉所有 WPD 的裝置服務。<br/>                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> </dl>

 

 




