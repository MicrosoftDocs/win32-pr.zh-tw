---
title: Win32_TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法
description: 藉由設定 UserAuthenticationRequired 屬性的值，啟用或停用使用者必須在連接時驗證的要求。
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- SetUserAuthenticationRequired 方法遠端桌面服務
- SetUserAuthenticationRequired 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetUserAuthenticationRequired 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317428"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Win32 TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法 \_

藉由設定 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)類別中 **UserAuthenticationRequired** 屬性的值，啟用或停用使用者必須在連接時驗證的要求。 若 **為 True**，表示已啟用， **UserAuthenticationRequired** 需要在連接時進行使用者驗證，以增加伺服器保護以防止網路攻擊。 只有支援 RDP 6.0 版或更高版本的遠端桌面通訊協定 (RDP) 用戶端才能連接。 為了避免遠端使用者中斷，建議您在啟用屬性之前，先部署支援適當通訊協定版本的 RDP 用戶端。

## <a name="syntax"></a>語法


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UserAuthenticationRequired* \[在\]
</dt> <dd>

指出是否需要使用者驗證。

<dt>

0 (0x0) 
</dt> <dd>

停用使用者必須經過驗證的需求

</dd> <dt>

1 (0x1) 
</dt> <dd>

啟用使用者必須經過驗證的需求。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

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
</dt> </dl>

 

