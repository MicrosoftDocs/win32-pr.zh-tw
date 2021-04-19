---
description: 使用者可以在安裝時，透過使用者介面或命令列來設定 MSIINSTALLPERUSER 和 ALLUSERS 屬性，以要求 Windows Installer 為目前的使用者或電腦的所有使用者安裝雙重用途的封裝。
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: MSIINSTALLPERUSER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998721"
---
# <a name="msiinstallperuser-property"></a>MSIINSTALLPERUSER 屬性

使用者可以在安裝時，透過使用者介面或命令列來設定 **MSIINSTALLPERUSER** 和 [**ALLUSERS**](allusers.md) 屬性，以要求 Windows Installer 為目前的使用者或電腦的所有使用者安裝雙重用途的封裝。 若要使用 **MSIINSTALLPERUSER** 屬性， [**ALLUSERS**](allusers.md) 屬性的值必須是2，而封裝必須經過撰寫，才能安裝到每位使用者或每一電腦的內容中。 如需撰寫雙重用途封裝的相關資訊，請參閱 [單一封裝撰寫](single-package-authoring.md)。 如果 **ALLUSERS** 屬性的值不等於2，就會忽略 **MSIINSTALLPERUSER** 屬性的值，而且不會影響安裝。 使用 Windows Installer 4.5 或更早版本安裝封裝時，會忽略 **MSIINSTALLPERUSER** 屬性的值。

若要要求 Windows Installer 在每部電腦 [安裝內容](installation-context.md)中安裝雙重用途套件，使用者可以使用撰寫的使用者介面或命令列，將 **MSIINSTALLPERUSER** 屬性的值設定為空字串 ( "" ) 以及 [**ALLUSERS**](allusers.md) 屬性的值設定為2。

若要要求 Windows Installer 在每個使用者 [安裝內容](installation-context.md)中安裝雙重用途封裝，使用者可以使用撰寫的使用者介面或命令列，將 **MSIINSTALLPERUSER** 屬性的值設定為1，並將 [**ALLUSERS**](allusers.md) 屬性的值設定為2。

如果 [**ALLUSERS**](allusers.md) 屬性的值不等於2，Windows Installer 會忽略 **MSIINSTALLPERUSER** 屬性的值。 如果 Windows Installer 將應用程式安裝在每部電腦的內容中，它會將 **ALLUSERS** 屬性的值重設為1。 如果 Windows Installer 將應用程式安裝在每個使用者的內容中，它會將 **ALLUSERS** 屬性的值重設為空字串 ( "" ) 。 針對每位使用者安裝的應用程式，會收到每個使用者的所有更新或修復，以及每部電腦安裝的應用程式每一電腦的更新或修復。

**[Windows Installer 4.5 或更早](not-supported-in-windows-installer-4-5.md)版本：** Windows Installer 5.0 之前的版本會忽略 **MSIINSTALLPERUSER** 屬性。

## <a name="default-value"></a>預設值

建議的預設安裝內容為每位使用者提供的雙重用途套件。 在雙重用途封裝的 [屬性工作表](property-table.md) 中，Author MSIINSTALLPERUSER = 1 和 ALLUSERS = 2，以指定每位使用者作為預設安裝內容。

## <a name="remarks"></a>備註

您可以將值設為空字串 ( "" ) ，MSIINSTALLPERUSER = ""，以確定尚未設定 **MSIINSTALLPERUSER** 屬性。

安裝內容會決定 [**DesktopFolder**](desktopfolder.md)、 [**ProgramMenuFolder**](programmenufolder.md)、 [**StartMenuFolder**](startmenufolder.md)、 [**StartupFolder**](startupfolder.md)、 [**TemplateFolder**](templatefolder.md)、 [**AdminToolsFolder**](admintoolsfolder.md)、 [**ProgramFilesFolder**](programfilesfolder.md)、 [**CommonFilesFolder**](commonfilesfolder.md)、 [**ProgramFiles64Folder**](programfiles64folder.md)和 [**CommonFiles64Folder**](commonfiles64folder.md) 屬性的值。 安裝內容會決定登錄的部分，其中登錄 [表](registry-table.md) 和 [RemoveRegistry 資料表](removeregistry-table.md)中的專案（在根資料行中為-1）會寫入或移除。 如需安裝內容的詳細資訊，請參閱 [安裝內容](installation-context.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[安裝內容](installation-context.md)
</dt> <dt>

[單一套件撰寫](single-package-authoring.md)
</dt> </dl>

 

 




