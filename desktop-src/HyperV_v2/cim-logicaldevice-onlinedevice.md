---
description: OnlineDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: CIM_LogicalDevice 類別的 OnlineDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988972"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>CIM LogicalDevice 類別的 OnlineDevice 方法 \_

**OnlineDevice** 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 **RequestStateChange** 方法。

## <a name="syntax"></a>語法


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*線上* \[在\]
</dt> <dd>

若 **為 TRUE**，請讓裝置上線，如果是 **FALSE**，則讓裝置離線。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




