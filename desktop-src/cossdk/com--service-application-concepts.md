---
description: COM + 服務應用程式概念
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: COM + 服務應用程式概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468120"
---
# <a name="com-service-application-concepts"></a>COM + 服務應用程式概念

您可以使用 [元件服務] 系統管理工具，將 COM + 伺服器應用程式設定為服務應用程式。 以服務方式執行 COM + 伺服器應用程式可提供下列優點：

-   如果您的應用程式一律需要執行，則元件服務可以選擇性地自動啟動伺服器，也可以在伺服器超時時重新開機伺服器。例如，如果執行已排入佇列之元件接聽程式元件的電腦重新開機，則已排入佇列的元件接聽程式如果設定為服務，就可以自動啟動。
-   如果您的應用程式需要執行特殊許可權的作業，應用程式可以執行為本機系統帳戶。 只有 NT 服務可使用此層級的安全性來執行。 應用程式將與 Windows 叢集服務相容，這會在系統容錯移轉期間管理服務。
-   如果其他服務需要標記為相依的，則元件服務會提供該選項。 例如，如果您的應用程式使用其他服務所提供的功能，則會在應用程式啟動之前啟動標示為相依的服務。

## <a name="starting-an-application-automatically"></a>自動啟動應用程式

當 COM + 伺服器應用程式自動啟動時，它的作用就像是服務，需要開發人員使用「服務」系統管理工具來管理伺服器。

> [!Note]  
> 您可以啟動 [元件服務] 系統管理工具，然後按一下 [ **服務] (本機)** 來存取服務系統管理工具。

 

## <a name="starting-an-application-manually"></a>手動啟動應用程式

當 COM + 伺服器應用程式以手動方式啟動時，它的作用就像是具有服務安全性設定的 DLL 主機。 服務會在啟動時以手動方式啟動，並在發生時自動關閉。

## <a name="service-configurations"></a>服務組態

無論啟動類型為何，您都可以將應用程式設定為以本機系統帳戶執行，或指派給使用者帳戶。 您可以在建立服務時設定本機系統和使用者帳戶。 若要設定安全性設定，必須使用「服務」系統管理工具。 也可以針對服務設定相依性。

您也可以從其他系統服務清單中選取 [相依性]，以任何特定順序啟動應用程式。 例如，系統服務可以標示為相依，而且在系統服務已依照指定的順序啟動之前，將不會啟動應用程式。 這會在使用服務應用程式之前，先將它初始化。

如需如何將 COM + 應用程式設定為以服務方式執行的逐步指示，請參閱將 [COM + 伺服器應用程式設定為服務應用程式](configuring-a-com--server-application-as-a-service-application.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 服務應用程式工作](com--service-application-tasks.md)
</dt> </dl>

 

 



