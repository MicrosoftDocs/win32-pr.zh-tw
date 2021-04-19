---
description: 此範例說明如何使用自訂轉換來停用功能並新增資源。
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: 自訂轉換範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993098"
---
# <a name="a-customization-transform-example"></a>自訂轉換範例

此範例說明如何使用自訂轉換來停用功能並新增資源。

系統管理員可以使用自訂轉換，在 [功能資料表](feature-table.md)的 [層級] 資料行中輸入0，以永久停用功能。 然後，如果使用者使用 UI 選取完整安裝，或在命令列上將 [ [**ADDLOCAL**](addlocal.md) ] 屬性設定為 [全部]，則應用程式的自訂轉換會防止安裝和顯示該功能。 如需安裝層級的討論，請參閱 [功能資料表](feature-table.md) 與 [**INSTALLLEVEL**](installlevel.md) 屬性。

您可以使用自訂轉換來部署自訂應用程式所需的資源，以新增一或多個新元件。 轉換必須加入一或多個新功能，以包含這些新元件。 如需部署資源（例如檔案、登錄機碼或快捷方式）時應遵循的規則，請參閱 [使用轉換來新增資源](using-transforms-to-add-resources.md)。

此範例說明如何建立 [轉換](transforms.md) 來自訂安裝 [範例](an-installation-example.md)中所述的應用程式安裝。 原始安裝套件會安裝範例應用程式的所有功能，包括功能閘道，可讓使用者查看 Red 公園的招生資訊。 某些使用者群組只需要提供事件排程資訊的應用程式功能，而且不需要閘道功能。 這些群組也需要取得特殊的電話清單。 因此轉換必須進行兩項作業： 1) 自訂安裝，讓此群組只會收到所需的應用程式功能，而 2) 為新的電話清單提供所需的資源。

此範例的最基本使用者介面範例，會在 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md) 中提供，做為檔 Uisample.msi。 如果您有 SDK，就可以存取重現範例安裝套件、使用者介面和自訂轉換所需的所有工具和資料。

自訂轉換具有下列規格：

-   自訂轉換內嵌于 MNP2000.msi 檔案中，以確保它一律可供安裝資料庫使用。
-   使用自訂轉換安裝 MNP2000.msi 不會安裝閘道功能、閘道功能的子功能，或是閘道功能的任何元件（即使使用者選取完整的安裝類型）。
-   其他應用程式可能會共用閘道功能的部分或全部元件。 這些應用程式的安裝套件可能會將其所有元件安裝在使用者的電腦上。
-   使用自訂轉換移除 MNP2000.msi 不會移除其他應用程式已安裝的任何閘道元件。
-   使用自訂轉換安裝 MNP2000.msi 也會安裝新的最上層功能、電話 \_ 清單，以及需要安裝資源的新元件電話，Phone.txt。 使用者會 \_ 使用功能表目錄中的快捷方式來存取電話清單功能。

[繼續](customizing-an-original-database.md)

 

 



