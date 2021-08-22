---
description: Windows在 Windows Server 2008 R2 或 Windows 7 上執行的安裝程式5.0 可以列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: 列舉元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598e80e270d0442b06fdb6db50cc5b58df529a1305936f2610211f192c8572be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947039"
---
# <a name="enumerating-components"></a>列舉元件

Windows在 Windows Server 2008 R2 或 Windows 7 上執行的安裝程式5.0 可以列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。 針對 Windows Installer 5.0 撰寫的封裝可以使用 [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)、 [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)和 [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)函式，在使用者帳戶和安裝內容之間搜尋元件和產品。 [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)、 [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)和 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)函式只會傳回針對呼叫函式之使用者帳戶所安裝之元件和產品的資訊。 針對每個使用者帳戶，多次呼叫這些函式至少需要一次，才能收集整個電腦的資訊。

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)函式會列舉已安裝的元件。 函式會在每次呼叫時，捕獲一個元件程式碼。 [**元件物件**](components.md)會透過此函式接收已安裝元件的相關資訊。

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)函式會列舉屬於指定已安裝元件之用戶端的產品。 [**用戶端物件**](client.md)會透過此函數接收用戶端的相關資訊。

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)函式會傳回已安裝元件的完整路徑。 如果元件的金鑰路徑是登錄機碼，則函式會傳回登錄機碼。 [**ComponentInfo 物件**](componentinfo.md)會透過此函式接收已安裝元件的相關資訊。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows 7 或 Windows Server 2008 R2 上執行的 Windows Installer 5.0 開始，可以使用這項功能。

 

 



