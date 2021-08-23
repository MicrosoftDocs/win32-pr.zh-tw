---
description: SetShareInfo&\# 8194;WMI 類別方法會設定共用資源的參數。
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Win32_Share 類別的 SetShareInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800898"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Win32 共用類別的 SetShareInfo 方法 \_

**SetShareInfo** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會設定共用資源的參數。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaximumAllowed* \[在中，選擇性\]
</dt> <dd>

允許同時使用此資源的使用者數目上限。

範例：10。 這是選擇性參數。

</dd> <dt>

*描述* \[在中，選擇性\]
</dt> <dd>

描述所共用資源的選擇性批註。

</dd> <dt>

*存取* \[在中，選擇性\]
</dt> <dd>

使用者層級許可權的安全描述項。 安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。 如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

**不正確名稱** (9) 
</dt> <dt>

**層級** (10) 無效
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**重複的共用** (22) 
</dt> <dt>

重新 **導向路徑** (23) 
</dt> <dt>

**未知的裝置或目錄** (24) 
</dt> <dt>

**找不到網路名稱** (25) 
</dt> <dt>

**其他** (26 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

**SetShareInfo** 方法是動態物件方法，會用於這個類別的出現位置。

只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行 **SetShareInfo**。 列印操作員只能設定印表機佇列。 通訊運算子只能設定通訊裝置佇列。

## <a name="examples"></a>範例

下列 PowerShell 範例會更新 **newShare** 共用的名稱。


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



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

[**Win32 \_ 共用**](win32-share.md)
</dt> </dl>

 

