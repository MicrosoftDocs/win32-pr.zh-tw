---
title: Win32_TSGeneralSetting 類別的 SetSecurityLayer 方法
description: SetSecurityLayer 方法會設定安全性層級。
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- SetSecurityLayer 方法遠端桌面服務
- SetSecurityLayer 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetSecurityLayer 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934475"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Win32 TSGeneralSetting 類別的 SetSecurityLayer 方法 \_

**SetSecurityLayer** 方法會設定安全性層級。

## <a name="syntax"></a>語法


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SecurityLayer* \[在\]
</dt> <dd>

要設定的安全性層級。 如果目前的加密層級為1，則 *SecurityLayer* 的值為2，表示無效。

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP 安全性層** (0) 


</dt> <dd>

伺服器和用戶端之間的通訊，會使用原生 RDP 加密。

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (1) 


</dt> <dd>

會使用用戶端可支援之最安全的安全性階層。 若支援 SSL (TLS 1.0)，就會使用 SSL (TLS 1.0)。

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2) 


</dt> <dd>

SSL (TLS 1.0) 將用於伺服器驗證，以及用來加密伺服器與用戶端之間傳送的所有資料。 此設定需要伺服器具有 SSL 相容的憑證。 這項設定與 **MinEncryptionLevel** 值1不相容。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

