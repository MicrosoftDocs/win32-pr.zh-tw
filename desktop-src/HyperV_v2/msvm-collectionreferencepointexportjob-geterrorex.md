---
description: Msvm_CollectionReferencePointExportJob 類別的 GetErrorEx 方法-抓取錯誤的其他相關資訊。
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Msvm_CollectionReferencePointExportJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112086"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Msvm CollectionReferencePointExportJob 類別的 GetErrorEx 方法 \_

抓取有關錯誤的其他資訊。 當作業正在執行或已終止而沒有錯誤時， **GetErrorEx** 會傳回沒有 [**Msvm \_ 錯誤**](msvm-error.md) 實例。 但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止工作，則 **GetErrorEx** 會傳回一或多個 **Msvm \_ 錯誤** 實例。

## <a name="syntax"></a>語法


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[擴展\]
</dt> <dd>

如果作業的操作狀態不是「確定」，這個參數會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例的陣列。 否則，如果作業為 "OK"，此參數會包含 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會傳回下列其中一個錯誤值：

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
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




