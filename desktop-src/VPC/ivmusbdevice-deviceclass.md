---
title: 'IVMUSBDevice DeviceClass 屬性 (VPCCOMInterfaces .h) '
description: 抓取 USB 裝置的裝置類別。
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- DeviceClass 屬性 Virtual PC
- DeviceClass 屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，DeviceClass 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385041"
---
# <a name="ivmusbdevicedeviceclass-property"></a>IVMUSBDevice：:D eviceClass 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取 USB 裝置的裝置類別。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>屬性值

裝置類別。 如需值的清單，請參閱 [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md)。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                            | 意義                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>               | 已成功完成命令。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl> | 參數為 **Null**。<br/>         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

