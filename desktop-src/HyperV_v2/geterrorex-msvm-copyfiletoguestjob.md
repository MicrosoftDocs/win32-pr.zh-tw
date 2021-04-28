---
description: Msvm_CopyFileToGuestJob：： GetErrorEx 方法-抓取作業的錯誤物件（如果有的話）。
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob：： GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109666"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a>Msvm \_ CopyFileToGuestJob：： GetErrorEx 方法

抓取作業的錯誤物件（如果有的話）。 當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。 但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。

## <a name="syntax"></a>語法


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[擴展\]
</dt> <dd>

如果作業的作業狀態不是 2 (確定) ，這個方法會傳回一或多個 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例（以 CIM XML 格式表示），表示工作中遇到的錯誤。 如果作業的操作狀態為 2 (確定) ，則會傳回 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**System 使用** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




