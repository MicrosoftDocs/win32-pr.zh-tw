---
description: 您可能偶爾需要判斷應用程式是否在 Tablet PC 上執行，因為您可能會想要讓您的應用程式利用固有的筆墨、辨識和畫筆功能。
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: 判斷電腦是否為 Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979313"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>判斷電腦是否為 Tablet PC

您可能偶爾需要判斷應用程式是否在 Tablet PC 上執行，因為您可能會想要讓您的應用程式利用固有的筆墨、辨識和畫筆功能。 為了協助您判斷您的應用程式是否能存取 Tablet PC 功能，您可以使用 GetSystemMetrics () Windows API 呼叫，如本主題中所述。

## <a name="client-side-applications"></a>Client-Side 應用程式

您可以使用下列技術，判斷您的程式碼是否在 Tablet PC 上執行。

-   [使用 GetSystemMetrics (SM \_ 平板) ](/windows)
-   [使用平板電腦平臺二進位檔的存在](#using-the-presence-of-tablet-platform-binaries)
-   [以 Web 為基礎的應用程式](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>使用 GetSystemMetrics (SM \_ 平板) 

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

在 Microsoft Windows XP Tablet PC Edition 中，請使用 GetSystemMetrics (SM \_ 平板電腦) 功能來判斷電腦是否為 TABLET PC。 GetSystemMetrics (SM \_ 平板電腦) 是設計成在執行 WINDOWS XP TABLET PC Edition 的電腦上回到 TRUE。

### <a name="windows-vista"></a>Windows Vista

在 Windows Vista 中，不再有不同的 Tablet PC SDK。 Windows SDK 現在包含一個稱為「Tablet PC 和觸控技術」的區段，而 GetSystemMetrics (SM 平板電腦) 的邏輯已 \_ 變更為反映這一點。 GetSystemMetrics (SM \_ 平板) 現在如果符合下列所有條件，則會傳回 true：

-   系統上有一個整合式數位板，也就是筆觸或觸控。
-   已安裝 Tablet PC 選用元件。 此元件包含 [Tablet PC 輸入面板] 和 [Windows 筆記本] 等功能。
-   電腦授權使用選用元件。 高階版本的 Windows Vista （像是 Windows Vista Home Premium、Windows Vista Small Business、Windows Vista Professional、Windows Vista Enterprise 和 Windows Vista 旗艦版）是授權使用選用元件。
-   Tablet PC 輸入服務正在執行。 Tablet PC 輸入服務是 Windows Vista 的新服務，可控制 Tablet PC 輸入。

利用這種提高的精確度，GetSystemMetrics (SM \_ 平板電腦) 繼續建議用來判斷執行 Windows Vista 的電腦是否為 TABLET PC。

### <a name="using-the-presence-of-tablet-platform-binaries"></a>使用平板電腦平臺二進位檔的存在

在 Windows XP Tablet PC Edition 和 Windows Vista 中，您可以搜尋筆墨二進位檔（例如 inkobj.dll 和 Microsoft.Ink.dll）是否存在，並使用其支援的功能（如果有的話）。

在 Windows Vista 中，預設會在所有的用戶端版本上安裝 Tablet PC 平臺二進位檔。 這些版本有提供輸入和筆跡功能。 辨識僅適用于 premium 版本的 Windows Vista。

### <a name="web-based-applications"></a>Web-Based 應用程式

在 Windows Vista 中，Internet Explorer 所報告的使用者代理程式字串包含 "Tablet PC 2.0"，如果根據 GetSystemMetrics (SM \_ 平板電腦) ，則裝置是 tablet pc。

在 Windows XP Tablet PC Edition 2005 中，使用者代理字串包含 Tablet PC 1.7。 使用者代理程式字串看起來像下面這樣：

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

您可以使用此值來判斷用戶端電腦是否為 Tablet PC，並支援以 Web 為基礎的筆墨控制項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
