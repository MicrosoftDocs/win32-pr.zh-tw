---
title: MSAD_DomainController 類別的 ExecuteKCC 方法
description: 呼叫 DsReplicaConsistencyCheck 函式，此函式會叫用知識一致性檢查程式 (KCC) 來確認複寫拓撲。
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- ExecuteKCC 方法 Active Directory
- ExecuteKCC 方法 Active Directory，MSAD_DomainController 類別
- MSAD_DomainController 類別 Active Directory，ExecuteKCC 方法
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969182"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>MSAD 控制器類別的 ExecuteKCC 方法 \_

呼叫 [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) 函式，此函式會叫用知識一致性檢查程式 (KCC) 來確認複寫拓撲。

## <a name="syntax"></a>語法


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TaskID* \[在\]
</dt> <dd>

KCC 應執行的工作。 **DS \_KCC \_ TASKID \_ 更新 \_ 拓撲** 是目前唯一支援的值。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

一組旗標，可修改 **ExecuteKCC** 方法的行為。 這個參數可以是零或一或多個下列值的組合。

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ 旗標 \_ 非同步 \_ OP**


</dt> <dd>

工作會排入佇列，然後函式會傳回，而不會等候工作完成。

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS \_ KCC \_ 旗標 \_ 禁止**


</dt> <dd>

如果有其他已排入佇列的工作即將執行，則工作不會新增至佇列。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSAD 的 \_ 控制器**](msad-domaincontroller.md)
</dt> </dl>

 

 





