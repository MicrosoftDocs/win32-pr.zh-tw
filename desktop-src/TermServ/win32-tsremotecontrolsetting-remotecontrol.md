---
title: Win32_TSRemoteControlSetting 類別的 RemoteControl 方法
description: RemoteControl 方法會設定 LevelOfControl 屬性。
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- RemoteControl 方法遠端桌面服務
- RemoteControl 方法遠端桌面服務，Win32_TSRemoteControlSetting 類別
- Win32_TSRemoteControlSetting 類別遠端桌面服務，RemoteControl 方法
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769418"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Win32 TSRemoteControlSetting 類別的 RemoteControl 方法 \_

**RemoteControl** 方法會設定 **LevelOfControl** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LevelOfControl* \[在\]
</dt> <dd>

**LevelOfControl** 屬性的新值，這個值會指定是否只由遠端使用者查看會話，或透過鍵盤和滑鼠來查看和控制會話。 如需詳細資訊，請參閱＜備註＞一節。 支援下列值。

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (0) 


</dt> <dd>

遠端控制已停用。

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1) 


</dt> <dd>

遠端控制的使用者可以完全掌控使用者的會話，以及使用者的許可權。

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2) 


</dt> <dd>

遠端控制的使用者可以完全掌控使用者的會話;不需要使用者的許可權。

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3) 


</dt> <dd>

遠端控制的使用者可以從遠端使用使用者的許可權來查看會話;遠端使用者無法主動控制會話。

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4) 


</dt> <dd>

遠端控制的使用者可以從遠端查看會話，但不能主動控制會話;不需要使用者的許可權。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="remarks"></a>備註

會話的完整控制權表示遠端使用者可以使用鍵盤和滑鼠主動控制使用者的會話。

當使用者嘗試建立遠端控制連線時，系統會顯示訊息給遠端用戶端，要求許可權，以在遠端會話中進行 view 或積極參與。

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

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

