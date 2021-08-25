---
description: 提供從 Microsoft 媒體基礎 video 轉譯接收器取得 IMFDXGIDeviceManager 的功能。
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: IMFDXGIDeviceManagerSource 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: c75b2a691bfe9fcbda453fd49a29fcfd2ff640346f0e3c13a34418995439f4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957848"
---
# <a name="imfdxgidevicemanagersource-interface"></a>IMFDXGIDeviceManagerSource 介面

提供從 Microsoft 媒體基礎 video 轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 的功能。

## <a name="members"></a>成員

**IMFDXGIDeviceManagerSource** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMFDXGIDeviceManagerSource** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMFDXGIDeviceManagerSource** 介面具有這些方法。



| 方法                                                      | 描述                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [**GetManager**](imfdxgidevicemanagersource-getmanager.md) | 從媒體基礎影片轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎介面](media-foundation-interfaces.md)
</dt> </dl>

 

 
