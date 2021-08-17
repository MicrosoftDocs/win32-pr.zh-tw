---
title: IMsRdpDeviceV2 IsUSBDevice 屬性
description: 指定裝置是否用於 USB 重新導向。
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- IsUSBDevice 屬性遠端桌面服務
- IsUSBDevice 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，IsUSBDevice 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03e2572912487cb924f65350dbdd7818d07d2a7b172d18cb28fab87335a00dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138561"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a>IMsRdpDeviceV2：： IsUSBDevice 屬性

指定裝置是否用於 USB 重新導向。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a>屬性值

如果裝置適用于 USB 重新導向，則 **為 true** ;否則 **為 false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 SP1<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 包含 SP1<br/>                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





