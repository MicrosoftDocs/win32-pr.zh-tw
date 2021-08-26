---
description: GDI 列印 API 中函式的其中一個主要功能是支援裝置獨立性。
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: 關於 GDI 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951008"
---
# <a name="about-the-gdi-print-api"></a>關於 GDI 列印 API

GDI 列印 API 中函式的其中一個主要功能是支援裝置獨立性。 應用程式不會發出裝置特定的命令以在特定印表機或繪圖器上繪製輸出，而是從圖形裝置介面呼叫高階函式 (GDI) 。 例如，若要列印點陣圖影像，應用程式可以呼叫 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 函式，並提供點陣圖的座標，以及識別來源和目的地裝置內容 (dc) 的控制碼。 然後，印表機驅動程式會將對 **BitBlt** 的呼叫轉換為原始裝置命令。 設備磁碟機是動態連結程式庫 (DLL) ，可支援 (DDI) 的設備磁碟機介面。 當設備磁碟機處理圖形引擎對 DDI 函式的呼叫時，會產生原始的裝置命令。 印表機會在列印影像時處理這些命令。 這些命令的語法、數目和類型會因裝置而異。

本總覽提供下列主題的相關資訊。

<dl>

[預設列印介面](default-printing-interface.md)  
[印表機裝置內容](printer-output.md)  
[印表機轉義](printer-escapes.md)  
[WYSIWYG 顯示和輸出](wysiwyg-display-and-output.md)  
[每位使用者的 DEVMODE](per-user-devmode.md)  
</dl>

 

 
