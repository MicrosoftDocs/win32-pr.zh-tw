---
description: QuiesceDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: CIM_LogicalDevice 類別的 QuiesceDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320099"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>CIM LogicalDevice 類別的 QuiesceDevice 方法 \_

**QuiesceDevice** 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 **RequestStateChange** 方法。

## <a name="syntax"></a>語法


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*靜止* \[在\]
</dt> <dd>

如果設定為 **TRUE** ，則會完全停止所有活動（如果 **為 FALSE** resume 活動）。

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

 

 




