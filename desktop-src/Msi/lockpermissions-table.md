---
description: 用來在鎖定的環境中保護應用程式的個別部分。 它可用於安裝檔案、登錄機碼和建立的資料夾。
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: LockPermissions 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992453"
---
# <a name="lockpermissions-table"></a>LockPermissions 資料表

LockPermissions 資料表是用來保護鎖定環境中應用程式的個別部分。 它可用於安裝檔案、登錄機碼和建立的資料夾。

適用于在 Windows Server 2008 R2 或 Windows 7 安裝的套件應該使用 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) ，而不是 LockPermissions 資料表。 Windows Installer Windows Installer 5.0 之前的版本會忽略 MsiLockPermissionsEx 資料表。 Windows Installer 5.0 可以安裝包含 LockPermissions 資料表的封裝。 從 Windows Installer 5.0 開始，安裝包含 MsiLockPermissionsEx 資料表和 LockPermissions 資料表的封裝會失敗，並傳回 Windows Installer 錯誤訊息1941。

LockPermissions 資料表具有下列資料行。



| Column     | 類型                               | 答案 | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [識別碼](identifier.md)       | Y   | N        |
| 資料表      | [Text](text.md)                   | Y   | N        |
| 網域     | [格式 化](formatted.md)         | Y   | Y        |
| User       | [格式 化](formatted.md)         | Y   | N        |
| 權限 | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

這個資料行和資料表資料行會指定要保護的檔案、目錄或登錄機碼。 LockObject 資料行是一個外鍵，指向資料表資料行所指定之資料表的主鍵。

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

這個資料行和 LockObject 資料行指定要保護的檔案、目錄或登錄機碼。 在 [資料表] 資料行中，輸入 File、Registry 或 CreateFolder，以指定檔案 [資料表](file-table.md)、登錄 [表](registry-table.md)或 [CreateFolder 資料表](createfolder-table.md)中所列的 LockObject。

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>域
</dt> <dd>

識別要設定許可權之使用者網域的資料行。 這是獨立電腦或功能變數名稱的名稱。 資料行資料類型已 [格式化](formatted.md)，您可以 \[ \] 在此欄位中使用字串% USERDOMAIN 來取得目前網域的 USERDOMAIN 環境變數值。 若要取得任何其他網域，則需要使用 [自訂動作](custom-actions.md)。 如需詳細資訊，請參閱自訂動作表。

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>使用者
</dt> <dd>

識別要設定許可權之使用者的當地語系化名稱的資料行。 此名稱必須位於電腦或網域上。 如果電腦或網域控制站無法辨識網域和使用者組合，或無法抓取 (SID) 使用者的安全識別碼，則安裝會失敗。 可以為單一 LockObject 指定多個使用者。

一般使用者名稱「Everyone」和「系統管理員」可能會以英文輸入，並對應到知名的 Sid。 LocalSystem 在透過 LockPermissions 資料表所建立的所有安全描述項中，都具有完整控制權。 您可以使用此欄位中的 [ [**ComputerName] 屬性**](computername.md)、[ [**LogonUser] 屬性**](logonuser.md) 或 [使用者名稱] [**屬性**](username.md) 來取得目前的使用者。 需要自訂動作，才能輸入任何其他使用者或群組的當地語系化名稱。

您可以使用具有相同 LockObject 和資料表專案的多筆記錄 (但) 不同的使用者專案，以指定多個使用者的存取控制清單。

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>許可
</dt> <dd>

識別系統許可權之整數描述的資料行。 以下提供最常使用的值 (在 Winnt. h) 中有完整清單。



| Privilege                                                              | Description                     |
|------------------------------------------------------------------------|---------------------------------|
| 一般 \_ 全部<br/> 0X10000000<br/> 268435456<br/>     | 讀取、寫入和執行存取權 |
| 一般 \_ 執行<br/> 0X20000000<br/> 536870912<br/> | 執行存取                  |
| 一般 \_ 寫入<br/> 0X40000000<br/> 1073741824<br/>  | 寫入存取權                    |



 

您無法 \_ 在許可權資料行中指定泛型 READ。 嘗試這麼做將會失敗。 相反地，您必須指定一個值，例如讀取金鑰 \_ 或 \_ 讀取檔案一般 \_ 。

在此資料行中輸入的 Null 已保留供日後使用。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallFiles](installfiles-action.md)、 [WriteRegistryValues](writeregistryvalues-action.md)和 [CreateFolders](createfolders-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

只有在已經存在於電腦或網域上的使用者，才能在 LockPermissions 資料表中設定許可權。 嘗試設定未知使用者的許可權，會導致安裝失敗，即使該使用者帳戶是在安裝期間由延遲的自訂動作所建立。

建議將系統管理員的本機群組包含在 (ACL) 的所有存取控制清單中。 這可確保系統管理員可以存取和維護物件。

LockPermissions 資料表中所列的每個檔案、登錄機碼或目錄都會收到明確的安全描述項（不論是否取代現有的物件）。 Windows Installer 會嘗試在已經存在於系統上的物件上保留安全性。 如果物件未列在 LockPermissions 資料表中，並取代現有的物件，則取代會取得它所取代之物件的安全性設定。

如果物件未列在 LockPermissions 資料表中，而且不會取代現有的物件，它就不會收到任何明確的安全描述項。 新物件的存取是以其父系或容器物件的屬性為基礎。 如果物件未列在資料表中，並將物件取代為沒有明確安全描述項的物件，則會根據其父系或容器物件的屬性來存取新的物件。

Windows Installer 將 [**UserSID**](usersid.md) 屬性設定為安全性識別元 (SID) 或執行安裝的使用者。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




