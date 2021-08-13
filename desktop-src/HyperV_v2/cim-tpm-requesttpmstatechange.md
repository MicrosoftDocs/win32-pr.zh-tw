---
description: 要求將 TPM 的狀態變更為 RequestedTPMState 參數中指定的值。
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: CIM_TPM 類別的 RequestTPMStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 94af1d619ffa686b2fb4546987c6b825e4c658a5ae045d84fe5c6181716e95e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646446"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>CIM TPM 類別的 RequestTPMStateChange 方法 \_

要求將 TPM 的狀態變更為 *RequestedTPMState* 參數中指定的值。 如果方法調用成功完成， **TPMState** 屬性應該等於 **RequestedTPMState** 參數。 多次叫用 **RequestTPMStateChange** 方法可能會導致較早的要求被覆寫或遺失。

## <a name="syntax"></a>語法


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedTPMState* \[在\]
</dt> <dd>

要求的 TPM 狀態。

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**已啟用 S1-Active-擁有的** (2) 


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 已停用-Active-擁有的** (3) 


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**已啟用 S3-非使用中-擁有的** (4) 


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**已停用 S4-非使用中-擁有的** (5) 


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**已啟用 S5-主動-** 無人擁有的 (6) 


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 已停用-主動-** 無人 (7) 


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 已啟用-非** 使用中-無人擁有的 (8) 


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 已停用-非** 使用中-無人擁有的 (9) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[在\]
</dt> <dd>

可能需要的授權權杖，動作才會生效。 可能需要 *AuthorizationToken* 參數，才能建立實體存在，或傳遞 OWNERAUTH （TCG 定義的擁有者授權密碼）。 在 OwnerAuth 的案例中， \_ 可能需要 cim SharedCredential （具有非 null 值的 cim \_ SharedCredential）。 CIM \_ SharedCredential 演算法屬性也可以根據屬性 cim \_ TPMCapabilities. SupportedPasswordAlgorithms 來指定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

可能包含建立之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 的參考，以追蹤方法調用所起始的狀態轉換。

</dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。 間隔格式必須用來指定 *TimeoutPeriod*。 值為0或 null 參數表示用戶端沒有轉換的時間需求。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回0或 4096;否則，會傳回錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未知或未指定的錯誤** (2) 
</dt> <dt>

**無法在 Timeout 期間內完成** (3) 
</dt> <dt>

**失敗** (4) 
</dt> <dt>

**不正確參數** (5) 
</dt> <dt>

**使用** (6) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**不正確狀態轉換** (4097) 
</dt> <dt>

 (4098) **不支援使用 Timeout 參數**
</dt> <dt>

**忙碌** (4099) 
</dt> <dt>

**方法保留** (4100. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
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

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




