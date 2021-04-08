---
title: 備份與還原 Active Directory 伺服器
description: Active Directory Domain Services 提供在目錄資料庫中備份和還原資料的功能。
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services、使用、備份和還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681695"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>備份與還原 Active Directory 伺服器

Active Directory Domain Services 提供在目錄資料庫中備份和還原資料的功能。 本節說明如何 [備份](backing-up-an-active-directory-server.md) 和 [還原](restoring-an-active-directory-server.md) Active Directory 的伺服器。 如需有關使用 Windows 2000 和 Windows Server 2003 作業系統中提供的公用程式來備份 Active Directory 伺服器的詳細資訊，請參閱 Microsoft TechNet 網站上的適用資源套件（英文）。

Active Directory 伺服器的備份必須在線上執行，而且必須在安裝 Active Directory Domain Services 時執行。 Active Directory Domain Services 是以特殊資料庫為基礎，並匯出一組提供程式設計備份介面的備份函式。 備份不支援增量備份。 備份應用程式會使用 Ntdsbcli 中定義的進入點，系結至本機用戶端 DLL。

Active Directory 伺服器的還原一律會離線執行。

雖然本節中的主題僅說明如何備份和還原 Active Directory 伺服器，但請注意，Windows 2000 和 Windows Server 2003 作業系統都有幾個必須同時備份和還原的「系統狀態」元件。 這些系統狀態元件包含：

-   開機檔案，例如 ntldr、ntdetect、由 SFP 保護的所有檔案，以及效能計數器設定
-   Active Directory 網網域控制站
-   只有) 的 SysVol (網域控制站
-   只有) 的憑證伺服器 (CA
-   叢集資料庫 (叢集節點僅) 
-   登錄
-   COM + 類別註冊資料庫

系統狀態可以依任何順序進行備份，但是系統狀態的還原必須依照下列順序進行：

1.  還原開機檔案。
2.  適當地還原 SysVol、憑證伺服器、叢集資料庫和 COM + 類別註冊資料庫。
3.  還原 Active Directory 的伺服器。
4.  還原登錄。

如需有關備份和還原憑證服務的詳細資訊，請參閱 [使用憑證服務備份和還原功能](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions)。

如需備份和還原 Active Directory Domain Services 的詳細資訊，請參閱：

-   [Active Directory Domain Services 備份的考慮](considerations-for-active-directory-domain-services-backup.md)
-   [備份 Active Directory 伺服器](backing-up-an-active-directory-server.md)
-   [還原 Active Directory 伺服器](restoring-an-active-directory-server.md)
-   [目錄備份功能](directory-backup-functions.md)

 

 