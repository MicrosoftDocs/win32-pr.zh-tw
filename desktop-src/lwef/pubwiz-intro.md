---
title: 發佈嚮導簡介
description: WindowsXP 引進了 Web 發佈嚮導和線上列印順序 Wizard。
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- 發佈嚮導，關於
- Web 發佈嚮導，關於
- 線上列印訂購嚮導，關於
- 發佈嚮導，Web 發佈嚮導
- 發佈嚮導，線上列印訂購嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d576d04579847d2e65bbc59399d11689259f8e64823a3c3068cafad912ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246665"
---
# <a name="publishing-wizards-introduction"></a>發佈嚮導簡介

WindowsXP 引進了 Web 發佈嚮導和線上列印順序 Wizard。 根據相同的架構，這些嚮導為使用者提供一個簡單的機制，可將內容發佈至網站，或訂購從數位影像檔進行的列印。 這些瀏覽器的優點在於能夠在其 wizard 頁面中裝載來自不同提供者的 HTML 內容，讓 [外觀]、[程式] 和 [可用] 使用者選項可以完全由提供者控制，而且可能會隨時變更，而不會影響裝載它們的用戶端 wizard。 雖然這些現有的嚮導都是以非常重要的數位影像來建立的，但架構和概念可用於許多其他用途，例如檔列印服務，或作為與朋友和家人共用影像的方法。

-   [它如何運作？](#how-does-it-work)
-   [發佈嚮導檔](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>它如何運作？

Web 發佈嚮導和線上列印順序 Wizard 的使用者體驗很類似，但每個 Wizard 的進入點各有不同。 若為 Web 發佈嚮導，標題為 [將 **此資料夾發佈到網站** ] 的工作，可以從大部分資料夾流覽的左側的 [檔案 **和資料夾** 工作] 清單中取得。 工作的文字會根據選取的內容而有所不同。 比方說，如果選取檔案，則工作會將 **這個檔案發佈到網站** ，如下列範例所示。

![檔案和資料夾工作](images/shell-pubwiz-tasks.png)

使用者按一下工作以啟動精靈。 繼續進行嚮導，使用者會看到提供者清單，如下列範例所示。 網際網路服務提供者 (Isp) 可以開發並註冊自己的提供者頁面，以顯示在此清單中。

![發佈嚮導提供者清單](images/shell-pubwiz-provs.png)

選擇提供者之後，嚮導會連線至該網站，而第一個 HTML 網頁的下載則會在嚮導中顯示。 如果使用者沒有所選提供者的帳戶，則會有機會設定一個。

在嚮導的單一頁面中包含多個 HTML 網頁;換句話說，裝載 procession HTML 網頁的 wizard 頁面的控制碼會維持不變。 HTML 頁面會在中央窗格中公開，就像任何標準的 wizard 頁面一樣。 提供者網站提供的方法，可控制在顯示 HTML 網頁時，wizard 的 [ **上一頁**]、 **[下一頁**] 和 [ **取消** ] 按鈕的出現位置。 在這些 HTML 網頁中，系統可能會要求使用者指定可複製檔案的資料夾，或儲存他們想要建立之網站的名稱。 當使用者完成所有必要的步驟之後，網站會呼叫方法來開始上傳，然後將控制權歸還給 wizard。 Wizard 本身會處理上傳和任何的任何附隨圖形，例如進度指標。 上傳完成之後，提供者網站可以指定 URL，讓使用者可以在關閉嚮導之後進行。

在 [線上列印順序] 嚮導中，工作 **順序** 只會在 [圖片] 資料夾（例如 [我的圖片]）中看到，如下列範例所示。 不過，此程式與 Web 發佈嚮導非常類似。 提供者網站會提示使用者提供選項，例如影像選取、列印大小、份數，以及付款資訊。

![圖片工作](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>發佈嚮導檔

下列檔將詳細討論 Web 發佈嚮導和線上列印順序的 Wizard。 此外，也會討論如何開發應用程式來裝載這些應用程式。

-   [用戶端設計](pubwiz-client.md)
-   [伺服器端設計](pubwiz-server.md)
-   [註冊服務](pubwiz-reg.md)
-   [使用傳送資訊清單](pubwiz-manifest.md)
-   [傳送資訊清單架構](/windows/desktop/shell/interfaces)

 

 