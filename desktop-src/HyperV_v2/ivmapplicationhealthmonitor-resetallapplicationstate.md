---
description: 重設虛擬機器中所有應用程式的健全狀況狀態。
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: IVmApplicationHealthMonitor：： ResetAllApplicationState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694348"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>IVmApplicationHealthMonitor：： ResetAllApplicationState 方法

重設虛擬機器中所有應用程式的健全狀況狀態。 如果成功，所有受監視應用程式的健全狀況狀態將會設定為 **ApplicationStateHealthy**。

## <a name="syntax"></a>語法


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                      |
| 版本<br/>                  | Windows 8 的整合元件<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




