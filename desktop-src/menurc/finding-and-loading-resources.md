---
title: 尋找和載入資源
description: 本主題討論如何將資源載入記憶體中。
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463000"
---
# <a name="finding-and-loading-resources"></a>尋找和載入資源

使用資源之前，應用程式必須將它載入記憶體中。 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea)和 [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)函數會尋找模組中的資源，並將控制碼傳回給二進位資源資料。 **FindResource** 會依類型和名稱來尋找資源。 **FindResourceEx** 會依類型、名稱和語言來尋找資源。 本主題中的 **FindResource** 相關資訊也適用于 **FindResourceEx**。

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)函式會使用 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea)所傳回的資源控制碼，將資源載入記憶體中。 應用程式使用 **LoadResource** 載入資源之後，只有在其模組的所有參考都透過 [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)釋放時，系統才會卸載相關聯的記憶體。 需要重複存取特定模組內相同或多個資源的應用程式，可能會因為在重複的 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 **FreeLibrary** 呼叫中發生記憶體對應而導致效能受到負面影響。 應用程式應該儲存單一模組控制碼，直到不再需要資源，然後再呼叫 **FreeLibrary**。 從記憶體卸載模組之後，資源控制碼會變成無效。

應用程式可以使用 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) 和 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 來尋找和載入任何類型的資源，但是這些函式只能在下列其中一種情況下使用：

-   當應用程式無法使用現有的資源特定功能來存取資源時。
-   當應用程式必須以二進位資料的形式存取資源，以進行後續的函式呼叫。

如果可能的話，應用程式應該改為使用下列其中一個資源特定的函式，在一個呼叫中尋找和載入資源：



| 函式                                     | 動作                                   | 移除資源                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | 載入並格式化訊息資料表專案。 | 不需採取動作。                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | 載入快速鍵對應表。              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | 載入點陣圖資源。                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | 載入資料指標資源。                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | 載入圖示資源。                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | 載入圖示、游標或點陣圖。        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)、 [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)、 [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | 載入功能表資源。                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**Loadstring 時**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | 載入字串資料表專案。              | 不需採取動作。                                                                                                |



 

請注意上表中的發行功能。 在終止之前，應用程式應該使用適當的函式來釋出快速鍵資料表、點陣圖、游標、圖示和功能表所佔用的記憶體。

透過 [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) 和 [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) 所載入之資源的相關記憶體，將會在該模組被 [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)的呼叫卸載之後釋放。 系統會自動釋放在應用程式終止時保持卸載的任何資源。

 

 