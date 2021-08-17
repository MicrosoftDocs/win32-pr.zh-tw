---
description: WMI 具有安全性常數，用於 \_ \_ SystemSecurity：： GetCallerAccessRights 的命名空間存取檢查。
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: '命名空間存取權限常數 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 6c23bcde9d085a6668fd5c57ee0ff51a7db61784de44d79080e2b2d2d1ee051f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992748"
---
# <a name="namespace-access-rights-constants"></a>命名空間存取權限常數

WMI 具有安全性常數，用於 [**\_ \_ SystemSecurity：： GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)的命名空間存取檢查。 如需存取控制清單 (Acl、Dacl 或 Sacl) 的安全性資訊，請參閱 [ (acl 的存取控制清單)](/windows/desktop/SecAuthZ/access-control-lists) 和 [**標準存取權限**](/windows/desktop/SecAuthZ/standard-access-rights)。 這些常數定義于 **WBEM \_ 安全性 \_ 旗標** 列舉中。

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ 啟用**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



啟用帳戶並授與使用者讀取權限。 這是所有使用者的預設存取權，並且對應至 [*WMI 控制項*](gloss-w.md)[安全性] 索引標籤上的 [啟用帳戶] 許可權。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ 方法 \_ 執行**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



允許執行方法。 提供者可以執行額外的存取檢查。 這是所有使用者的預設存取權，並且對應至 WMI 控制項 [安全性] 索引標籤上的 [執行方法] 許可權。


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ 完整 \_ 寫入 \_ 代表**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



允許使用者帳戶寫入 WMI 存放庫和實例中的類別。 使用者無法寫入系統類別。 只有 Administrators 群組的成員具有此許可權。 **WBEM \_FULL \_ write \_ REP** 對應于 WMI 控制項 [安全性] 索引標籤的完整寫入權限。


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ 部分 \_ 寫入 \_ 代表**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



可讓您將資料寫入至實例，而不是類別。 使用者無法將類別寫入 WMI 存放 [*庫*](gloss-w.md)。 只有 Administrators 群組的成員才有這個許可權。 **WBEM \_部分 \_ 寫入的 \_ 代表** 會對應至 WMI 控制項 [安全性] 索引標籤的部分寫入權限。


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ 寫入 \_ 提供者**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



允許將類別和實例寫入提供者。 請注意，提供者可以在模擬使用者時進行額外的存取檢查。 這是所有使用者的預設存取權，並且對應至 WMI 控制項 [安全性] 索引標籤的提供者寫入權限。


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ 遠端 \_ 訪問**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



允許使用者帳戶從遠端執行上述許可權所允許的任何作業。 只有 Administrators 群組的成員才有這個許可權。 **WBEM \_[遠端 \_ 訪問** ] 對應至 WMI 控制項 [安全性] 索引標籤上的 [遠端啟用] 許可權。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wbemcli。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

[存取 WMI 命名空間](access-to-wmi-namespaces.md)
</dt> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> <dt>

[變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

