---
description: '遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) '
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: '遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10af070d54dceebe51f9872b3b58c42467040d5ad8f24f593774576b159cbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645738"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊) 

## <a name="affected-platforms"></a>受影響的平臺

**伺服器**– Windows server 2008 \| Windows server 2008 R2  

## <a name="description"></a>描述

遠端桌面服務 (之前稱為終端機服務) 可讓多個並行使用者存取 Windows 伺服器，以便使用 Microsoft 「展示虛擬化」技術提供應用程式和資料裝載服務。

雖然大部分的32位和64位應用程式都是以 Windows 遠端桌面服務的方式執行，但因為平臺 (多使用者環境的差異，所以會有數個其他使用者的平行存取，以及) 的平行存取。

如需有關應用程式品質的詳細資訊，請參閱 *適用于終端機服務的應用程式就緒* 白皮書。 造訪遠端桌面服務產品頁面，TS TechNet 網站深入瞭解遠端桌面服務。 若要深入瞭解如何開發遠端桌面服務的應用程式，請參閱 *終端機服務程式設計指導方針*。  (這些資源可能無法在某些語言及國家/地區使用。 ) 

## <a name="manifestation-of-impacts-and-their-mitigations"></a>影響因素及其緩和措施的表現

Windows 7 的三項變更會影響遠端桌面服務上的應用程式：

-   WindowsServer 2008 R2 僅限64位
-   每一會話 IP 虛擬化
-   以 MSI 為基礎的部署–使用者特定的金鑰

**僅限64位 Windows Server 2008 R2**

針對32位伺服器撰寫的應用程式將以 WoW 模式執行，而不是在 Windows server 2008 R2 上以原生方式執行，因此遠端桌面服務。 如需詳細資訊，請參閱 Windows 僅限 7 64 位的主題。

*64位的緩和措施 Windows Server 2008 R2*

大部分針對32位撰寫的應用程式在 WoW 模式下將繼續正常運作。 針對 Windows 7 遠端桌面服務撰寫的任何新應用程式，都應該針對64位平臺上的部署進行開發和測試。

**IP 虛擬化**

遠端桌面 IP 虛擬可讓使用者在每個會話或個別程式上，將 IP 位址指派給遠端桌面連線：

-   如果您在每個會話上指派 IP 位址，則所有應用程式都會使用會話 IP 位址。
-   如果您以個別程式為基礎指派 IP 位址，則只有指定的應用程式會使用會話 IP 位址，而且會話中的其餘應用程式不會受到影響。
-   如果您指派多個程式的 IP 位址，它們會共用會話 IP 位址。
-   如果電腦上有一個以上的網路介面卡，您也必須選擇其中一個網路介面卡進行遠端桌面 IP 虛擬。

*IP 虛擬化的緩和措施*

某些程式需要每個應用程式實例都有唯一的 IP 位址。 在 Windows Server 2008 R2 之前，遠端桌面伺服器上的每個會話都會共用相同的 IP 位址，而導致這些應用程式的相容性問題。 遠端桌面 IP 虛擬可讓這些應用程式在遠端桌面伺服器上執行。

**以 MSI 為基礎的部署**

Microsoft Installer RDS 相容性是 Windows Server 2008 R2 中遠端桌面服務隨附的新功能。 使用 Windows Server 2008 R2 中的遠端桌面服務時，會由遠端桌面伺服器將每個使用者的應用程式安裝排入佇列，然後由 Microsoft 安裝程式進行處理。

在 Windows Server 2008 R2 中，您可以在遠端桌面伺服器上安裝程式，就像在本機桌面上安裝程式一樣。 不過，請確定您為所有使用者安裝程式，並在遠端桌面伺服器本機上安裝程式的所有元件。

*以 MSI 為基礎的部署緩和措施*

在 Windows Server 2008 R2 版遠端桌面服務之前，Windows 一次只支援一個 Windows Installer 安裝。 對於需要個別使用者設定的應用程式（例如 Microsoft Office Word），系統管理員必須先安裝應用程式，而應用程式開發人員需要在遠端桌面用戶端和遠端桌面工作階段主機上測試這些應用程式。 Windows安裝程式 RDS 相容性功能可讓您同時識別和安裝多個使用者遺失的每個使用者設定，並讓應用程式安裝體驗與本機桌面上的遠端桌面伺服器類似。

**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md)角色的 Windows Server 2008 R2：** 不支援。 如果啟用[遠端桌面服務](../termserv/terminal-services-portal.md)角色，使用[MsiEmbeddedChainer 資料表](../msi/msiembeddedchainer-table.md)的多個套件安裝將會失敗。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [終端機服務程式設計指導方針](../termserv/terminal-services-programming-guidelines.md)
-   [終端機服務產品首頁](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [適用于終端機服務的應用程式就緒白皮書](/collaborate/connect-redirect)

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
