---
title: 啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式
description: 啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316582"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

Windows Store 應用程式使用者體驗一次著重在單一應用程式，其中包含多工、應用程式切換，以及 Windows UI 提供的通知。 Windows Store 應用程式會調整大小以填滿螢幕上的可用空間，最常見的觀點是全螢幕。 因此，當系統上的另一個應用程式啟動時，您就無法再假設新的應用程式會在桌面應用程式中開啟。 這永遠適用于選擇參與新的 Windows UI 體驗的 Windows Store 應用程式和瀏覽器。 您可以同時繼續查看其他應用程式，例如，如果您在桌面上，然後啟動另一個桌面應用程式，或者您的應用程式處於已貼齊的狀態。

## <a name="manifestation"></a>表現

當傳統型應用程式使用一般的應用程式啟用技術，例如在檔案或通訊協定上使用 ShellExecute API 時，Windows 會啟動與該註冊相關聯的應用程式，這可能是 Windows Store 應用程式及/或使用者的預設網頁瀏覽器 (預設的網頁瀏覽器可能會選擇參與桌面或新的 Windows UI) 。 Windows Store 應用程式是使用全螢幕來啟動，隱藏桌面以及從中啟動的桌面應用程式。

> [!Note]  
> 在 Windows 8 中，Internet Explorer 10 已設定為使用者的預設瀏覽器，但使用者可以選擇安裝並設定另一個瀏覽器，做為預設 (不會變更 Windows 7) 。 在 Internet Explorer 10 中，從桌面應用程式開啟連結時，會在桌面上開啟 Internet Explorer。 但使用者可以變更此設定，讓 Internet Explorer 以 Windows Store 應用程式的形式開啟。 我們鼓勵瀏覽器廠商採用類似的「內容啟動」體驗;不過，開發人員應該規劃不是所有瀏覽器的行為都同樣的事實。

 

## <a name="mitigation"></a>降低

雖然開發人員無法對其應用程式進行任何變更，以減輕這種行為，但一般使用者可以執行哪些動作，讓您可以進行通訊。 請考慮使用擴充 ShellExecuteEx () API 所收集的資訊來填入內容適當的對話方塊。 在該對話方塊中，向使用者指出將會啟動哪個應用程式，以及該應用程式是 Windows Store 應用程式還是桌面應用程式。 您可以使用 CLSID 來區別 Windows Store 應用程式與桌面應用程式。 使用者選項：

-   具有全螢幕監視器的使用者可以將 Windows Store 應用程式貼齊螢幕邊緣，以公開桌面，同時同時查看 Windows Store 應用程式和桌面應用程式。
-   如果 Internet Explorer 已設定為使用者的預設瀏覽器，則使用者可以變更控制台中的網際網路選項來變更其行為。 在 [程式] 索引標籤上，使用者可以變更 Internet Explorer 處理連結的方式。 其他瀏覽器可能會提供類似的設定。

 

 




