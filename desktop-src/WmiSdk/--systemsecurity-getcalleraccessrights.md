---
description: 將 rights 參數設定為點陣圖，每個位都對應至存取權限。
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetCallerAccessRights 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 770a4a51a6a0ea9e38e8c5bd6fed944b473a41373933cee497e98fd8f9952422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110023"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>\_ \_ SystemSecurity 類別的 GetCallerAccessRights 方法

**\_ \_ SystemSecurity：： GetCallerAccessRights** 方法會將 *許可權* 參數設定為點陣圖，每個位都對應至存取權限。 任何用戶端都可以呼叫這個來判斷用戶端擁有的許可權。 此方法適用于啟用或停用功能的用戶端。 例如，如果目前登入的使用者沒有方法執行許可權，GUI 應用程式可能會停用按鈕。

任何啟用的用戶端都有呼叫 **GetCallerAccessRights** 的許可權，即使該用戶端沒有一般方法執行許可權也一樣。

## <a name="syntax"></a>語法


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*權利* \[擴展\]
</dt> <dd>

用戶端的存取權限。 如需詳細資訊，請參閱 [**\_ \_ SystemSecurity**](--systemsecurity.md)和 [WMI 安全性常數](wmi-security-constants.md)。

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_啟用** (1 (0x1) ) 


</dt> <dd>

啟用帳戶並授與使用者讀取權限。 這是所有使用者的預設存取權限。

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_方法 \_ 執行** (2 (0x2) ) 


</dt> <dd>

允許執行方法。

> [!Note]  
> 提供者可能會執行額外的存取檢查。

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_FULL \_ WRITE \_ REP** (4 (0x4) ) 


</dt> <dd>

允許呼叫者、安全性內容或使用者寫入類別和實例（系統類別除外）。

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_部分 \_ 寫入 \_ 代表** (8 (0x8) ) 


</dt> <dd>

允許呼叫者、安全性內容或使用者將提供者實例（而非靜態類別或靜態實例）寫入存放庫。

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ (16 (0x10 寫入 \_ 提供者**) ) 


</dt> <dd>

允許呼叫者、安全性內容或使用者將類別和實例寫入提供者。

> [!Note]  
> 模擬提供者可能會進行額外的存取檢查。

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_遠端 \_ 訪問** (32 (0x20) ) 


</dt> <dd>

允許使用者帳戶從遠端執行其他位所設定之許可權所允許的任何作業。

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) 


</dt> <dd>

允許對安全描述項的讀取權限。

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) 


</dt> <dd>

允許對 (DACL) 的任意存取控制清單進行寫入存取。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。 下列清單列出對 [**Set9XUserList**](--systemsecurity-set9xuserlist.md)而言很重要的傳回值。 針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果[ReturnValue](parsing-outparameters-objects.md)。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

<dl> <dt>

**\_ \_ \_ 已停用 WBEM E 方法**
</dt> <dd>

Windows 支援的版本不支援這個方法。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

WMI 安全性常數
</dt> </dl>

 

