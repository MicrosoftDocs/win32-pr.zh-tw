---
description: 在某些情況下，不是系統管理員的使用者只能覆寫受限制 Windows Installer 公用屬性的核准清單。
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: 受限制的公用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af09200f10261e50564ae79dbad961474d23d8a6354cee7344aa107c8b73fb57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979298"
---
# <a name="restricted-public-properties"></a>受限制的公用屬性

在受控安裝的情況下，封裝作者可能需要限制哪些 [公用屬性](public-properties.md) 會傳遞至伺服器端，並且可由非系統管理員的使用者進行變更。 當安裝要求安裝程式需要使用較高的許可權時，通常需要一些限制才能維護安全的環境。 如果符合下列所有條件，則不是系統管理員的使用者只能覆寫受限制公用屬性的核准清單：

-   系統 Windows 2000。
-   使用者不是系統管理員。
-   正在以較高的許可權安裝應用程式或產品。

如果上述所有條件都成立，則安裝程式會預設為可由任何使用者變更的下列受限制公用屬性清單：

-   [**行動**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NOCOMPANYNAME**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**補丁**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**重新 啟動**](reboot.md)
-   [**REINSTALL**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**恢復**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**變換**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

安裝套件的作者可以使用 [**SecureCustomProperties**](securecustomproperties.md) 屬性，擴充此預設清單以包含其他公用屬性。

設定 [**EnableUserControl**](-enableusercontrol.md) 屬性或 [EnableUserControl](enableusercontrol.md)[系統原則](system-policy.md) 會將清單延伸至所有公用屬性。 然後，所有使用者都可以變更任何公用屬性。

每當非系統管理員使用者傳遞給伺服器的公用屬性清單受到限制時，安裝程式就會設定 [**RestrictedUserControl**](restrictedusercontrol.md) 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> </dl>

 

 



