---
title: 'IVMUSBDevice HubID 屬性 (VPCCOMInterfaces .h) '
description: 抓取裝置所連接之中樞的識別碼。
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- HubID 屬性 Virtual PC
- HubID 屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，HubID 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d36047722206c2dfd52f4fc14c8e98270db4cab2d62f0694ea3f44bac10449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958707"
---
# <a name="ivmusbdevicehubid-property"></a>IVMUSBDevice：： HubID 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取裝置所連接之中樞的識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a>屬性值

中樞識別碼。 此值是由 USB 連接器驅動程式所指派。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                            | 意義                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>               | 已成功完成命令。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl> | 參數為 **Null**。<br/>         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

