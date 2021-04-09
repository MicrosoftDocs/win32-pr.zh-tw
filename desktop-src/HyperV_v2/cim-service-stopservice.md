---
description: 步調處于已停止狀態的服務。
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: 'CIM_Service 類別的 StopService 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848163"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>CIM_Service 類別的 StopService 方法 (Hyper-v 管理) 

步調處于已停止狀態的服務。

> [!Note]
>
> 這個方法的語法與繼承自 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)的 **RequestStateChange** 方法重迭。 因為此方法已廣泛實行，所以會維護此方法，且其簡單的「停止」語義很方便使用。

 

## <a name="syntax"></a>語法


```mof
uint32 StopService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




