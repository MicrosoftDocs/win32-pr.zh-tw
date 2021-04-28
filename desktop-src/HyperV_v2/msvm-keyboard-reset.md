---
description: 重設 Msvm_Keyboard 類別的方法-重設虛擬鍵盤。
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Msvm_Keyboard 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 14c3166ce57fab4693dec87d3d81a55f1f688aa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111706"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a>Msvm 鍵盤類別的 Reset 方法 \_

重設虛擬鍵盤。

## <a name="syntax"></a>語法


```mof
uint32 Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回值為零表示成功。 傳回值為1表示失敗，因為不支援此方法。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ 鍵盤**](msvm-keyboard.md)
</dt> </dl>

 

 




