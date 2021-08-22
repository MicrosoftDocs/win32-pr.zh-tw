---
description: 定義單一回呼方法。
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: 'IConnectionRequestCallback 介面 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 53e1549767c8577507b3126b3a293dfe4e523612809c144ff24c04dce4ab1ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697416"
---
# <a name="iconnectionrequestcallback-interface"></a>IConnectionRequestCallback 介面

**IConnectionRequestCallback** 介面會定義單一回呼方法。 Windows 的可攜式裝置 (WPD) 應用程式會將這個選擇性元件物件模型 (COM) 介面，以接收已完成要求的通知，以及解除擱置的要求。 要求會使用 [**IPortableDeviceConnector：：連線**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect)和 [**IPortableDeviceConnector：:D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)方法來傳送。

## <a name="members"></a>成員

**IConnectionRequestCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IConnectionRequestCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IConnectionRequestCallback** 介面具有這些方法。



| 方法                                                      | 描述                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | 通知應用程式先前已排程的要求已完成。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



 

