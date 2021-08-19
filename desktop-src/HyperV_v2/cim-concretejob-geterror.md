---
description: 抓取由於作業失敗所造成的錯誤。
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: CIM_ConcreteJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813264"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>CIM ConcreteJob 類別的 GetError 方法 \_

抓取由於作業失敗所造成的錯誤。 當作業正在執行或已終止但沒有錯誤時，此方法不會傳回任何 [**CIM \_ 錯誤**](cim-error.md) 實例。 但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回 **CIM \_ 錯誤** 實例。

## <a name="syntax"></a>語法


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[擴展\]
</dt> <dd>

如果作業的 **OperationalStatus** 不是「確定」，則傳回 [**CIM \_ 錯誤**](cim-error.md)實例，否則會傳回 **null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未指定的錯誤** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**失敗** (4) 
</dt> <dt>

**不正確參數** (5) 
</dt> <dt>

**拒絕存取** (6) 
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

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

 




