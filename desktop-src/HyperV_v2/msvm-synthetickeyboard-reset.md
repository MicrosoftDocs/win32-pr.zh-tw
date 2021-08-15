---
description: 重設 Msvm_SyntheticKeyboard 類別的方法-重設虛擬鍵盤。
ms.assetid: 2a943dd8-3b94-4b20-8786-7f9d8b0aeaa6
title: Msvm_SyntheticKeyboard 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7b519177c604ccd7017e8007715672d2cbcd0e101230efd191aaec3c0d8d90d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392046"
---
# <a name="reset-method-of-the-msvm_synthetickeyboard-class"></a>Msvm SyntheticKeyboard 類別的 Reset 方法 \_

重設虛擬鍵盤。

## <a name="syntax"></a>語法


```mof
uint32 Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會傳回錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




