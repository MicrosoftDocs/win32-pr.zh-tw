---
description: 只有當字型是在指定的裝置上，或安裝在系統字型資料表中時，應用程式才能使用字型來繪製文字。
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: 字型安裝和刪除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0184054973c769462ed8c1620e5534ff909576ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991234"
---
# <a name="font-installation-and-deletion"></a>字型安裝和刪除

只有當字型是在指定的裝置上，或安裝在系統字型資料表中時，應用程式才能使用字型來繪製文字。 字型資料表是內部陣列，可識別應用程式可用的所有 nondevice 字型。 應用程式可以藉由呼叫 [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 或 [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) 函式，來取得目前安裝在裝置上或儲存在內部字型資料表中的字型名稱。

若要暫時安裝字型，請呼叫 [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) 或 [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)。 這些函式會載入儲存在字型資源檔中的字型。 不過，這是暫時性的安裝，因為在重新開機後，將不會出現字型。

若要安裝系統重新開機後仍會保留的字型，請使用下列其中一種方法：

-   移至主控台，按一下 [字型 **] 圖示，** 然後 **從 [檔案**] 功能表選取 [**安裝新** 字型]。 即使在重新開機之前，應用程式也可以使用字型。 不過，在終端機伺服器的情況下，字型適用于目前的會話，但在重新開機之前無法供其他會話使用。
-   將字型複製到% windir% \\ fonts 資料夾。 然後，移至主控台並按一下 **字型圖示，** 或呼叫 [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) 或 [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa)。 即使在重新開機之前，應用程式也可以使用字型。 不過，在終端機伺服器的情況下，字型適用于目前的會話，但在重新開機之前無法供其他會話使用。 如果您只將字型複製到% windir% 字型 \\ 資料夾，則只有在系統重新開機之後，才可以使用字型。

當應用程式使用已安裝的字型完成時，必須呼叫 [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 函數來移除該字型。

在 \\ 任何使用中的會話載入（包括會話0）時，無法修改從% windir% 字型資料夾以外的位置安裝的字型。 因此將會封鎖任何變更、取代或刪除的嘗試。 如果需要修改字型：

-   *暫時* 字型只會在目前的會話中載入。 嘗試修改任何字型之前，請先呼叫 [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 來強制目前的會話卸載字型。
-   *永久* 字型會在重新開機後繼續安裝，而且會由所有建立的會話載入。 呼叫 [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 來強制目前的會話卸載字型。 然後，在字型登錄機碼 (**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\** 字型) 尋找和移除與字型相關聯的登錄值。 最後，重新開機電腦，以確保不會在任何會話中載入字型。 重新開機之後，請繼續進行您的字型修改/刪除。

每當應用程式呼叫新增和刪除字型資源的函式時，它也應該呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式，並將 [**WM \_ FONTCHANGE**](wm-fontchange.md) 訊息傳送至系統中的所有最上層視窗。 這則訊息會通知其他應用程式，其內部字型資料表已由新增或移除字型的應用程式更改。

 

 
