---
description: 裝置獨立性是 Microsoft Windows 的主要功能之一。
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: 關於裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b686ec8b48492658f19531cb42161c043f178d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114244"
---
# <a name="about-device-contexts"></a>關於裝置內容

裝置獨立性是 Microsoft Windows 的主要功能之一。 應用程式可以在各種裝置上繪製和列印輸出。 支援此裝置獨立性的套裝軟體含在兩個動態連結程式庫中。 第一個是 Gdi.dll，稱為「圖形裝置介面」， (GDI) ;第二個稱為設備磁碟機。 第二個名稱會取決於應用程式繪製輸出的裝置。 例如，如果應用程式在 VGA 顯示器上的視窗工作區中繪製輸出，此程式庫會 Vga.dll;如果應用程式在 Epson FX-80 印表機上列印輸出，則會 Epson9.dll 此程式庫。

應用程式必須通知 GDI 載入特定的設備磁碟機，並在載入驅動程式之後，準備裝置以進行繪製作業 (例如選取線條色彩和寬度、筆刷模式和色彩、字型字型、裁剪區域等) 。 這些工作是藉由建立和維護裝置內容 (DC) 來完成。 DC 是一種結構，它會定義一組繪圖物件和其相關聯的屬性，以及影響輸出的圖形模式。 繪圖物件包括用來繪製線條的畫筆、繪製和填滿的筆刷、用來複製或滾動螢幕元件的點陣圖、定義可用色彩集的調色板、用於裁剪的區域、其他作業，以及繪製和繪製作業的路徑。 不同于大部分的結構，應用程式永遠不會直接存取 DC;相反地，它會藉由呼叫各種函式，間接地在結構上運作。

本總覽提供下列主題的相關資訊：

-   [繪圖物件](graphic-objects.md)
-   [圖形模式](graphic-modes.md)
-   [裝置內容類型](device-context-types.md)
-   [裝置內容作業](device-context-operations.md)
-   [具備 ICM 功能的裝置內容函式](icm-enabled-device-context-functions.md)

有一個重要的概念是 DC 或視窗的版面配置，其描述從左至右或由右至左) 顯示 GDI 物件和 (文字的順序。 如需詳細資訊，請參閱 [**視窗功能**](../winmsg/window-features.md) 和 [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) 和 [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) 函式中的「視窗版面配置和鏡像」。

 

 
