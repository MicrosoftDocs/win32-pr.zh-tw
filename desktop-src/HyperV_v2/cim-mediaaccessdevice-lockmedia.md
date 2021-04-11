---
description: 鎖定並解除鎖定可移動存取裝置中的媒體。
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: CIM_MediaAccessDevice 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027639"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a>CIM MediaAccessDevice 類別的 LockMedia 方法 \_

鎖定並解除鎖定可移動存取裝置中的媒體。

## <a name="syntax"></a>語法


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*鎖定* \[在\]
</dt> <dd>

若 **為 TRUE**，則會鎖定媒體。 如果 **為 FALSE**，則會釋放媒體。

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

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




