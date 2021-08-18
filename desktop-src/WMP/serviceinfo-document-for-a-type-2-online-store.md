---
title: 適用于 Type 2 線上商店的 ServiceInfo 檔
description: 適用于 Type 2 線上商店的 ServiceInfo 檔
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995428"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>適用于 Type 2 線上商店的 ServiceInfo 檔

Type 2 線上商店提供者必須為 Microsoft 提供描述線上商店之 XML 檔的 URL。 Windows Media Player 10 和 Windows Media Player 11 使用這份檔來決定如何設定使用者介面來裝載線上商店。

在 Windows Media Player 10 中，ServiceInfo 檔提供下列各項：

-   有關如何設定當線上商店處於作用中時，Windows Media Player 顯示的工作窗格的資訊。 線上商店可以有一個、兩個或三個工作窗格。
-   用來設定工作窗格按鈕的資訊，例如按鈕文字、按鈕色彩，以及按鈕的工具提示。
-   Windows Media Player 顯示以識別線上商店的影像 url。
-   線上商店提供的網頁 url，Windows Media Player 裝載于其使用者介面中。
-   Windows Media Player 安裝程式應該如何設定使用者看到的第一個線上商店的相關資訊。

在 Windows Media Player 11 中，ServiceInfo 檔提供下列各項：

-   用來設定 [線上商店] 索引標籤之按鈕的資訊，例如按鈕文字和按鈕的工具提示。
-   Windows Media Player 顯示以識別線上商店的影像 url。
-   線上商店提供的網頁 url，Windows Media Player 裝載于其使用者介面中。

當您開始開發線上商店時，必須向 Microsoft 提供 ServiceInfo 檔的 URL。 在開發階段，只有在設定特殊登錄機碼時，您的線上商店才會出現在 Windows Media Player 中。

在您的線上商店發佈之後，ususal 案例是 Windows Media Player 會自動從 Web 抓取您的 ServiceInfo 檔。 不過，在某些情況下，Windows Media Player 會從使用者的電腦抓取 ServiceInfo 檔。 如需詳細資訊，請參閱 [設定初始線上商店](setting-the-initial-online-store.md)。

當 Windows Media Player 從 Web 抓取 ServiceInfo 檔時，會將查詢字串附加至 URL。 查詢字串包含的參數可提供使用者地區設定和 Windows Media Player 版本的相關資訊。

您可以建立靜態或動態 ServiceInfo 檔。 靜態 ServiceInfo 檔具有 .xml 的副檔名。 動態 ServiceInfo 檔是 ASP 網頁，而且副檔名為 .asp 或 .aspx。

並非所有可在 ServiceInfo 檔中使用的元素都可供每個線上商店使用，而某些元素對於所有線上商店都是選擇性的。 如需您可以建立的線上商店類型，以及每種類型可用功能的相關資訊，請參閱[Windows Media Player 線上商店](windows-media-player-online-stores.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Type 2 線上商店**](about-type-2-online-stores.md)
</dt> <dt>

[**動態建立 ServiceInfo 檔**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 




