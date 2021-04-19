---
description: MsiLockPermissionsEx 資料表可以用來保護服務、檔案、登錄機碼和建立的資料夾。
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: MsiLockPermissionsEx 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997916"
---
# <a name="msilockpermissionsex-table"></a>MsiLockPermissionsEx 資料表

MsiLockPermissionsEx 資料表可以用來保護服務、檔案、登錄機碼和建立的資料夾。

封裝不應同時包含 MsiLockPermissionsEx 資料表和 [LockPermissions 資料表](lockpermissions-table.md)。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 針對要使用 Windows Installer 5.0 或更新版本安裝的套件，建議使用此資料表。

MsiLockPermissionsEx 資料表具有下列資料行。



| Column               | 類型                                       | 答案 | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | Y   | N        |
| LockObject           | [識別碼](identifier.md)               | N   | N        |
| 資料表                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| 條件            | [Condition](condition.md)                 | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

這是此資料表的主要索引鍵。

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

這個資料行和資料表資料行會指定要保護的檔案、目錄、登錄機碼或服務。 LockObject 資料行是一個外鍵，指向資料表資料行所指定之資料表的主鍵。

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

這個資料行和 LockObject 資料行指定要保護的檔案、目錄、登錄機碼或服務。 在 [資料表] 資料行中，輸入 File、Registry、CreateFolder 或 ServiceInstall，以指定檔案 [資料表](file-table.md)、登錄 [資料表](registry-table.md)、 [CreateFolder 資料表](createfolder-table.md)或 [ServiceInstall 資料表](serviceinstall-table.md)中所列的 LockObject。

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

輸入 SDDL 字串，表示要套用至所選物件的許可權。 您必須在 [安全描述項字串格式](../secauthz/security-descriptor-string-format.md)中提供 SDDL。

這不支援私用或公用屬性。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

此資料行包含條件運算式，用來判斷是否要套用指定的許可權。 如果條件評估為 **FALSE**，則不會套用許可權。 如果條件評估為 **TRUE**，則會套用許可權。

</dd> </dl>

## <a name="remarks"></a>備註

如需保護服務、檔案、登錄機碼和已建立資料夾的詳細資訊，請參閱 [保護資源](securing-resources-.md)。

使用 MsiLockPermissionsEx 資料表來保護安裝期間所建立之使用者帳戶的物件。 當安裝保護物件時，使用者帳戶必須已經存在。 在安裝檔案、登錄機碼、資料夾或服務受保護之前，請先建立使用者帳戶。

如果這個資料表中的 LockObject 和資料表配對有一個以上的條件運算式評估為 true，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1942。

如果 SDDLText 欄位中的 [FormattedSDDLText](formattedsddltext.md) 字串無法解析為有效的 SDDL 字串，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1943。

如果使用者沒有足夠的許可權可設定檔案或資料夾上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1926。

如果使用者沒有足夠的許可權可設定登錄機碼上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1401。

如果使用者沒有足夠的許可權可設定服務上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1944。

## <a name="validation"></a>驗證

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
