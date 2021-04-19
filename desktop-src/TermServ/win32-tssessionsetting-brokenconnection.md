---
title: 'Win32_TSSessionSetting 類別的 BrokenConnection 方法 (Wtsprotocol) '
description: 設定 BrokenConnectionAction 屬性，這是當達到會話時間限制或連接中斷時，伺服器所採取的動作。
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- BrokenConnection 方法遠端桌面服務
- BrokenConnection 方法遠端桌面服務，Win32_TSSessionSetting 類別
- Win32_TSSessionSetting 類別遠端桌面服務，BrokenConnection 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966308"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Win32 TSSessionSetting 類別的 BrokenConnection 方法 \_

設定 **BrokenConnectionAction** 屬性，這是當達到會話時間限制或連接中斷時，伺服器所採取的動作。

## <a name="syntax"></a>語法


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BrokenConnectionAction* \[在\]
</dt> <dd>

採取的動作。

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**中斷** (0) 


</dt> <dd>

使用者已與會話中斷連線。

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (1) 


</dt> <dd>

從伺服器中永久刪除會話。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則 control 下，方法會傳回錯誤。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Wtsprotocol。h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

