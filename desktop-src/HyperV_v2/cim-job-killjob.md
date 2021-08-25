---
description: 終止此作業和任何基礎進程，以及移除任何無關聯關聯的方法。 這個方法已被取代;請改用 RequestChangeState。
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: CIM_Job 類別的 KillJob 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 681d6a878f90f29708812fce2c39f27024ed588deb5f3b8066cc4833487fd91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900328"
---
# <a name="killjob-method-of-the-cim_job-class"></a>CIM 作業類別的 KillJob 方法 \_

終止此作業和任何基礎進程，以及移除任何「無關聯」關聯的方法。 這個方法已被取代;請改用 **RequestChangeState** 。 **KillJob** 即將被取代，因為有條理的關機和立即終止之間並沒有差別。 [**CIM \_ConcreteJob**](cim-concretejob.md)。**RequestStateChange** () 提供「終止」和「終止」選項，以允許這種差異。

## <a name="syntax"></a>語法


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DeleteOnKill* \[在\]
</dt> <dd>

指出作業是否應該在終止時自動刪除。 此參數優先于 **DeleteOnCompletion** 屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未知** 的 (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**失敗** (4) 
</dt> <dt>

**拒絕存取** (6) 
</dt> <dt>

**找不到** (7) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

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

[**CIM \_ 作業**](cim-job.md)
</dt> </dl>

 

 




