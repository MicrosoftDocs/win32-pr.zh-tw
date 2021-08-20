---
title: Win32_TSEnvironmentSetting 類別的 InitialProgram 方法
description: InitialProgram 方法會將啟動程式的屬性（例如名稱、工作目錄和程式的路徑）設定為在登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器之後立即啟動。
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- InitialProgram 方法遠端桌面服務
- InitialProgram 方法遠端桌面服務，Win32_TSEnvironmentSetting 類別
- Win32_TSEnvironmentSetting 類別遠端桌面服務，InitialProgram 方法
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d13aaa0e4dfb4e0d16bea89bf871a7a890c0f375fd928e70fd99aed20c003be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126987"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Win32 TSEnvironmentSetting 類別的 InitialProgram 方法 \_

**InitialProgram** 方法會將啟動程式的屬性（例如名稱、工作目錄和程式的路徑）設定為在登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器之後立即啟動。

## <a name="syntax"></a>語法


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InitialProgramPath* \[在\]
</dt> <dd>

啟動程式的名稱和路徑。

</dd> <dt>

*Startin* \[在\]
</dt> <dd>

啟動程式之工作目錄的路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

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

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

