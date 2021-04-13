---
title: SystemRestore 類別的 CreateRestorePoint 方法
description: 建立還原點。
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- CreateRestorePoint 方法系統還原
- CreateRestorePoint 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，CreateRestorePoint 方法
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465593"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>SystemRestore 類別的 CreateRestorePoint 方法

建立還原點。

這個方法是可編寫腳本的 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 函式對等專案。

## <a name="syntax"></a>語法


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[在\]
</dt> <dd>

要顯示的描述，讓使用者可以輕鬆地識別還原點。 ANSI 字串的最大長度為最大 \_ DESC。 Unicode 字串的最大長度為最大 \_ DESC \_ W。 如需詳細資訊，請參閱 [還原點描述文字](restore-point-description-text.md)。

</dd> <dt>

*RestorePointType* \[在\]
</dt> <dd>

還原點的類型。 這個成員可以是下列其中一個值。



| 還原點類型                                                                                                                                                                                                                             | 意義                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**應用程式 \_安裝**</dt> <dt>0</dt> </dl>         | 已安裝應用程式。<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**應用程式 \_卸載**</dt> <dt>1</dt> </dl>   | 已卸載應用程式。<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**裝置 \_驅動程式 \_ 安裝**</dt> <dt>10</dt> </dl> | 已安裝設備磁碟機。<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**修改 \_設定**</dt> <dt>12</dt> </dl>                    | 應用程式已新增或移除功能。<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> 已 <dt>**取消 \_操作**</dt> <dt>13</dt> </dl>        | 應用程式必須刪除它所建立的還原點。 例如，當使用者取消安裝時，應用程式會使用此旗標。<br/> |



 

</dd> <dt>

*事件* \[ 的在\]
</dt> <dd>

事件的類型。 這個成員可以是下列其中一個值。



| 事件類型                                                                                                                                                                                                                                                      | 意義                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**開始 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>102</dt> </dl> | 系統變更已開始。 後續的嵌套呼叫不會建立新的還原點。 <br/> 後續呼叫必須使用 END \_ NESTED \_ 系統 \_ 變更，而不是終端 \_ 系統 \_ 變更。<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**開始 \_系統 \_ 變更**</dt> <dt>100</dt> </dl>                       | 系統變更已開始。 <br/> 後續呼叫必須使用終端 \_ 系統 \_ 變更，而不是結束的 \_ 嵌套 \_ 系統 \_ 變更。<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**結束 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>103</dt> </dl>       | 系統變更已結束。<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**結束 \_系統 \_ 變更**</dt> <dt>101</dt> </dl>                             | 系統變更已結束。<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。 否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。

## <a name="remarks"></a>備註

* * Windows 8： * *

新的登錄機碼可讓應用程式開發人員變更還原點建立的頻率。

應用程式應該建立此金鑰來使用它，因為它不會在系統中之外。 如果機碼不存在，則預設會套用下列各項。 如果應用程式呼叫 **CreateRestorePoint** 方法來建立還原點，則 Windows 會在過去24小時內建立任何還原點時，略過建立這個新的還原點。 **CreateRestorePoint** 方法會傳回 **S \_ OK**。

開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **SystemRestorePointCreationFrequency** 。 此登錄機碼的值可以變更還原點建立的頻率。 此登錄機碼的值可以變更還原點建立的頻率。

如果應用程式呼叫 **CreateRestorePoint** 來建立還原點，而登錄機碼值為0，則系統還原不會略過建立新的還原點。

如果應用程式呼叫 **CreateRestorePoint** 來建立還原點，而登錄機碼值是整數 n，則系統還原會在前 N 分鐘內建立任何還原點時，略過建立新的還原點。

## <a name="examples"></a>範例


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                         |
| 命名空間<br/>                | 根 \\ 預設值<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr-iov</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





