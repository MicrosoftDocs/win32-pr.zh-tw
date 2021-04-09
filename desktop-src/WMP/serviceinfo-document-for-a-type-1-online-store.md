---
title: 類型1線上商店的 ServiceInfo 檔
description: 類型1線上商店的 ServiceInfo 檔
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021595"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>類型1線上商店的 ServiceInfo 檔

輸入1線上商店必須為 Microsoft 提供描述線上商店之 XML 檔的 URL。 Windows Media Player 11 使用這份檔來決定如何設定使用者介面來裝載線上商店。

類型1存放區的 ServiceInfo 檔提供下列資訊給 Windows Media Player：

-   用來設定 [ **線上商店** ] 按鈕的資訊 (也稱為索引標籤) ，例如按鈕文字、按鈕色彩，以及按鈕的工具提示。
-   Windows Media Player 顯示以識別線上商店的影像 Url。
-   線上商店提供的網頁 Url，Windows Media Player 裝載于其使用者介面中。
-   URL，其中 Windows Media Player 可以取得線上商店的外掛程式，以便將外掛程式安裝在使用者的電腦上。

當 Windows Media Player 從 Web 抓取 ServiceInfo 檔時，會將查詢字串附加至 URL。 查詢字串包含的參數可提供使用者地區設定和地理位置以及 Windows Media Player 版本的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**動態建立 ServiceInfo 檔**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 




