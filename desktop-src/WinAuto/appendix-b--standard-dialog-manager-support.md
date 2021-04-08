---
title: 附錄 B 標準對話方塊管理員支援
description: Microsoft Active Accessibility 提供標準對話方塊管理員 (SDM) 對話方塊控制項的完整支援。
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673444"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>附錄 B：標準對話方塊管理員支援

Microsoft Active Accessibility 提供標準對話方塊管理員 (SDM) 對話方塊控制項的完整支援。 SDM 是 Microsoft 的內部程式碼程式庫，可為 Microsoft 應用程式提供與 Macintosh 和 Microsoft Windows 作業系統之間的差異程度的獨立性。 SDM 主要用於 Microsoft Excel 和 Microsoft Word 中的對話方塊。

SDM 會顯示協助工具協助工具的問題，因為它使用了非標準的對話方塊。 例如，[SDM] 對話方塊按鈕不會使用 windows 控制碼，與標準使用者介面元素的方式相同。 您無法將訊息傳送至視窗清單中未包含的按鈕和按鈕。 使用 SDM 的應用程式會透過私用介面與控制項通訊。

下圖顯示 Word 的範例對話方塊。 雖然它看起來像是使用索引標籤控制項的一般 Windows 對話方塊，但它其實是一個 SDM 對話方塊。

![選取 [視圖] 索引標籤之 [選項] 對話方塊的螢幕擷取畫面](images/dialog.gif)

 

 




