---
description: 系統管理員可以使用下列方法，讓非系統管理員使用者以提高的系統許可權安裝應用程式。
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: 以較高的許可權安裝非系統管理員的封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603d2a39fd20a6ae2971a29e615887041e2a1fbf64989e93d5a1046f96102b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946106"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>以較高的許可權安裝非系統管理員的封裝

系統管理員可以使用下列方法，讓非系統管理員使用者以提高的系統許可權安裝應用程式。

-   在 Windows Installer 的 Windows Vista 中，系統管理員群組的成員可以提供授權給非系統管理員，以透過 [*使用者帳戶控制*](u-gly.md) (uac) 來提高安裝的許可權，如搭配 [使用 Windows Installer 和 uac](using-windows-installer-with-uac.md)所述。

    **Windows Vista：** 必填。

您也可以使用下列方法，以較高的系統許可權安裝應用程式。

-   系統管理員可以使用應用程式部署和[群組原則](/previous-versions/windows/desktop/Policy/group-policy-start-page)來指派或發佈 Windows Installer 套件，以公告使用者電腦上的應用程式。 系統管理員會針對每部電腦安裝通告套件。 如果非系統管理員使用者接著安裝應用程式，則可以使用較高的許可權來執行安裝。 非系統管理員的使用者無法安裝需要較高系統許可權的 unadvertised 套件。
-   系統管理員可以移至使用者的電腦，並針對個別電腦的安裝 [公告](advertisement.md) 應用程式。 由於 Windows Installer 一律具有更高的許可權，而且在個別電腦[安裝內容](installation-context.md)中執行安裝時，如果非系統管理員使用者接著安裝已公告的應用程式，則可以使用較高的許可權來執行安裝。 非系統管理員的使用者仍然無法安裝需要較高許可權的 unadvertised 套件。
-   如果本機系統代理程式通告應用程式，則沒有許可權的使用者可以安裝需要較高許可權的已公告應用程式。 您可以針對每個使用者或個別電腦的安裝來公告應用程式。 使用此方法安裝的應用程式會被視為受管理。 如需詳細資訊，請參閱 [廣告以較高的許可權安裝的 Per-User 應用程式](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)。
-   系統管理員可以針對每位使用者和每部電腦的安裝設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則。 這個方法可以開啟電腦的安全性風險，因為當設定此原則時，非系統管理員的使用者可以使用較高的許可權執行安裝，並存取電腦上的安全位置，例如 SystemFolder 或 **HKLM** 登錄機碼。

    如果在設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則的情況下，每一部電腦都已安裝應用程式，則會將產品視為受管理。 在此情況下，如果移除原則，應用程式仍然可以使用較高的許可權來執行修復。 此外，如果在設定 AlwaysInstallElevated 原則的情況下，每位使用者都安裝應用程式，則應用程式在移除原則時將無法執行修復。

-   系統管理員可以移至使用者的電腦，並執行應用程式的每一電腦安裝。 由於需要許可權才能執行這種類型的安裝，因此一律會管理每部電腦安裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安裝內容](installation-context.md)
</dt> </dl>

 

 
