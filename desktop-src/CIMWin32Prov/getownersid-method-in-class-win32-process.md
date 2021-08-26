---
description: GetOwnerSid&\# 8194;WMI 類別方法會針對此進程的擁有者，抓取 (SID) 的安全識別碼。
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetOwnerSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2884c0f1cd3cc6e32a2db1ab14824ba3112624002cb10f4d76782d622e069000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918378"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Win32 進程類別的 GetOwnerSid 方法 \_

**GetOwnerSid** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會針對此進程的擁有者，抓取 (SID) 的安全識別碼。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Sid* \[擴展\]
</dt> <dd>

傳回這個進程的安全識別碼描述元。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**許可權不足** (3) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

 (9) **找不到路徑**
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**其他** (22 4294967295) 
</dt> </dl>

## <a name="examples"></a>範例

[ [尋找遠端系統上的已登入的使用者2版](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) ] PowerShell 程式碼範例會查詢遠端電腦，以查看已登入的使用者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> </dl>

 

