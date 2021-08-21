---
title: 游標
description: 本節討論視窗工作區中的閃爍線、區塊或點陣圖游標。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- 資源，游標
- 游標，關於
- 閃爍線
- 閃爍的區塊
- 閃爍的點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed77a9d7fe315f5cef1be501c6392cce5fcfc3e79c5994f197a9fe6e254d8f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734851"
---
# <a name="carets"></a>游標

*插入* 點是視窗工作區中的閃爍線、區塊或點陣圖。 插入號通常表示將插入文字或圖形的位置。

下圖顯示插入點外觀的一些常見變化。

![顯示五種不同的插入號可以出現方式。](images/cscrt-01.png)

應用程式可以建立插入號、變更其閃爍時間，以及顯示、隱藏或重新放置插入號。

### <a name="in-this-section"></a>本節內容



| 名稱                                   | 描述                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [關於游標](about-carets.md)       | 討論游標。<br/>                                              |
| [使用游標](using-carets.md)       | 示範如何執行與游標相關之工作的程式碼範例。<br/> |
| [插入號參考](caret-reference.md) | 包含 API 參考。<br/>                                    |



 

### <a name="caret-functions"></a>插入號函式



| 名稱                                           | 描述                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | 建立系統插入號的新圖形，並將插入號的擁有權指派給指定的視窗。 插入號圖形可以是線條、區塊或點陣圖。 <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | 終結插入號的目前圖形，從視窗釋出插入號，然後從畫面中移除插入號。 <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | 抓取將插入號的圖元進行反轉所需的時間。 使用者可以設定此值。 <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | 將插入號的位置複製到指定的 [**點**](/previous-versions//dd162805(v=vs.85)) 結構。 <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | 從畫面移除插入號。 隱藏插入號不會終結其目前的形狀或使插入點失效。 <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | 將插入號閃爍時間設定為指定的毫秒數。 閃爍時間是反轉插入號圖元所需的經過時間（以毫秒為單位）。 <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | 將插入點移至指定的座標。 如果擁有插入號的視窗是使用 **CS \_ OWNDC** 類別樣式所建立，則指定的座標會受限於與該視窗相關聯之裝置內容的對應模式。 <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | 讓插入號顯示在畫面上插入號的目前位置。 當插入號變成可見時，它會自動開始閃爍。 <br/>                                                                                                          |



 

 

