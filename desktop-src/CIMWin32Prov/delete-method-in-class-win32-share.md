---
description: 從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Win32_Share 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918468"
---
# <a name="delete-method-of-the-win32_share-class"></a>Win32 共用類別的 Delete 方法 \_

**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Delete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

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

**Delete** 方法是物件方法，用於類別的實例。

只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行方法。 列印操作員只能刪除印表機佇列。 通訊運算子只能刪除通訊裝置佇列。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會刪除指定的共用。


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



下列 PowerShell 程式碼範例會刪除空白的共用。


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
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

 

