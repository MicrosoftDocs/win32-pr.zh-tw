---
title: RedirectDeviceType 列舉
description: 用來指定裝置的類型。
ms.assetid: B6356217-814E-462F-9DBC-F6D3C0CE129F
ms.tgt_platform: multiple
keywords:
- RedirectDeviceType 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- RedirectDeviceType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7058313e7f987589ae17924cce6a95610d997ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966108"
---
# <a name="redirectdevicetype-enumeration"></a>RedirectDeviceType 列舉

用來指定裝置的類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  UsbDevice  = 0
} RedirectDeviceType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="UsbDevice"></span><span id="usbdevice"></span><span id="USBDEVICE"></span>**UsbDevice**
</dt> <dd>

USB 裝置。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AddDeviceByInstanceId**](imsrdpdevicecollection2-adddevicebyinstanceid.md)
</dt> <dt>

[**RedirectNow**](imsrdpdevicecollection2-redirectnow.md)
</dt> </dl>

 

 





