---
Description: ALLUSERS 屬性會設定封裝的安裝內容。
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS 屬性
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987831"
---
# <a name="allusers-property"></a>ALLUSERS 屬性

**ALLUSERS** 屬性會設定封裝的安裝內容。 Windows Installer 會根據使用者的存取權限來執行每個使用者安裝或個別電腦安裝、是否需要較高的許可權才能安裝應用程式、 **ALLUSERS** 屬性的值、 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值和作業系統版本。

在安裝時， **ALLUSERS** 屬性的值會決定 [安裝內容](installation-context.md)。

-   **ALLUSERS** 屬性值1會指定每部電腦的安裝內容。
-   空字串 ( "" ) 指定每個使用者安裝內容的 **ALLUSERS** 屬性值。
-   如果 **allusers** 屬性的值設定為2，Windows Installer 一律會將 **allusers** 屬性的值重設為1，然後執行每一電腦安裝，或是將 **allusers** 屬性的值重設為空字串 ( "" ) 並執行每個使用者安裝。 ALLUSERS = 2 的值可讓系統重設 **allusers** 的值和安裝內容，取決於使用者的許可權和 Windows 版本。

    **Windows 7：** 將 **ALLUSERS** 屬性設定為2，即可使用 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性來指定安裝內容。 針對每部電腦安裝，將 **MSIINSTALLPERUSER** 屬性設定為空字串 ( "" ) 。 針對每個使用者安裝，將 **MSIINSTALLPERUSER** 屬性設定為1。 如果封裝已依照 [單一套件撰寫](single-package-authoring.md)中所述的開發指導方針撰寫，則擁有使用者存取權的使用者可以安裝到每個使用者的內容中，而不需要提供 UAC 認證。 如果使用者具有使用者存取權限，則只有在 [UAC] 對話方塊中提供系統管理員認證時，安裝程式才會執行個別電腦安裝。

    **Windows Vista：** 將 **ALLUSERS** 屬性設定為2，Windows Installer 符合 (UAC) 的 [*使用者帳戶控制*](u-gly.md) 。 如果使用者具有使用者存取權限，以及 ALLUSERS = 2，則安裝程式只會在提供系統管理員認證給 UAC 對話方塊時執行每部電腦安裝。 如果啟用 UAC 且未提供正確的系統管理員認證，則安裝會失敗並出現錯誤，指出需要系統管理員許可權。 如果登錄機碼、群組原則或控制台停用 UAC，則不會顯示 UAC 對話方塊，且安裝會失敗，並出現錯誤訊息，指出需要系統管理員許可權。

    **WINDOWS XP：** 如果使用者具有使用者存取權限，請將 **ALLUSERS** 屬性設定為2，Windows Installer 執行每個使用者安裝。

-   如果 **ALLUSERS** 屬性的值不等於2，Windows Installer 會忽略 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值。

## <a name="example"></a>範例

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) 取得的範例。

## <a name="default-value"></a>預設值

建議的預設安裝內容為每位使用者。 如果未設定 **ALLUSERS** ，安裝程式會執行每個使用者安裝。 您可以將值設為空字串 ( "" ) ，ALLUSERS = ""，以確定尚未設定 **ALLUSERS** 屬性。

## <a name="remarks"></a>備註

[安裝內容](installation-context.md)會決定 [**DesktopFolder**](desktopfolder.md)、 [**ProgramMenuFolder**](programmenufolder.md)、 [**StartMenuFolder**](startmenufolder.md)、 [**StartupFolder**](startupfolder.md)、 [**TemplateFolder**](templatefolder.md)、 [**AdminToolsFolder**](admintoolsfolder.md)、 [**ProgramFilesFolder**](programfilesfolder.md)、 [**CommonFilesFolder**](commonfilesfolder.md)、 [**ProgramFiles64Folder**](programfiles64folder.md)和 [**CommonFiles64Folder**](commonfiles64folder.md)屬性的值。 安裝內容會決定登錄的部分，其中登錄 [表](registry-table.md) 和 [RemoveRegistry 資料表](removeregistry-table.md)中的專案（在根資料行中為-1）會寫入或移除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[安裝內容](installation-context.md)
</dt> <dt>

[單一套件撰寫](single-package-authoring.md)
</dt> </dl>

 

 




