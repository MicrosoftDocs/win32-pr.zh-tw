---
title: 核心物件命名空間
description: 遠端桌面服務針對核心物件使用多個命名空間;全域命名空間主要是由用戶端/伺服器應用程式中的服務所使用。
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e1064638844039091dbe93aa1fedc75cb93f4aa1d012f8864e0154673c6cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989078"
---
# <a name="kernel-object-namespaces"></a>核心物件命名空間

遠端桌面服務伺服器有多個命名空間，適用于下列命名核心物件：事件、信號、mutex、可等候計時器、檔案對應物件和工作物件。 主要是由用戶端/伺服器應用程式中的服務所使用的全域命名空間。 此外，每個用戶端會話對於這些物件都有個別的命名空間，例如 Windows Vista 中。

不同的用戶端會話命名空間可讓多個用戶端執行相同的應用程式，而不會干擾彼此。 針對在用戶端會話下啟動的進程，系統預設會使用會話命名空間。 不過，這些進程可以在物件名稱前面加上 "Global" 前置詞，以使用全域命名空間 \\ 。 例如，下列程式碼會呼叫 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) ，並在全域命名空間中建立名為 CSAPP 的事件物件：

> [!Note]  
> 全域命名空間不適用於 Windows Store 應用程式。

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

遠端桌面服務環境中的服務應用程式預設會使用全域命名空間。

會話零隻用於裝載服務，且沒有主控台會話，與舊版 Windows 不同。

全域命名空間可讓多個用戶端會話上的進程與服務應用程式進行通訊。 例如，用戶端/伺服器應用程式可能會使用 mutex 物件進行同步處理。 伺服器模組可以在全域命名空間中建立 mutex 物件。 然後，用戶端會話可以使用 "Global \\ " 前置詞來開啟 mutex 物件。

全域命名空間的另一個用法是，應用程式使用命名物件來偵測在所有會話的系統中已經有應用程式的實例。 您必須在全域命名空間中建立或開啟這個命名物件，而不是每個會話的命名空間。 由於命名物件是在每個會話命名空間中建立，因此預設會支援每個會話執行一次應用程式的較常見案例。

除了 "Global \\ " 前置詞之外，用戶端進程還可以使用 "Local \\ " 前置詞，在其會話命名空間中明確建立物件。 這些關鍵字會區分大小寫。

「會話」 \\ 前置詞保留供系統使用，而且您不應該將它用於核心物件的名稱。

使用遠端桌面服務會話可執行快速切換使用者。 第一個登入的使用者會使用會話一，下一次登入的使用者會使用會話二，依此類推。 核心物件名稱必須遵循遠端桌面服務所述的指導方針，讓應用程式能夠支援多個使用者。

從會話零以外的會話使用 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)，在全域命名空間中建立檔案對應物件是具有特殊許可權的作業。 因此，在任意遠端桌面工作階段主機 (RD 工作階段主機) 伺服器會話中執行的應用程式必須啟用 [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) ，才能成功地在全域命名空間中建立檔案對應物件。 許可權檢查僅限於建立檔案對應物件，並不適用于開啟現有的物件。 例如，如果服務或系統建立檔案對應物件，則任何在任何會話中執行的進程都可以存取該檔案對應物件，前提是使用者具有必要的存取權。

 

 