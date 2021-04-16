---
title: 關於 DDEML
description: 本主題討論動態資料交換。
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (的 DDE) ，關於
- DDE (動態資料交換) ，關於
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) ，關於
- DDEML (動態資料交換管理程式庫) ，關於
- '資料交換、動態資料交換管理程式庫 (DDEML) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507448"
---
# <a name="about-the-ddeml"></a>關於 DDEML

動態資料交換 (的 DDE) 與剪貼簿資料傳輸機制不同。 其中一個差異是剪貼簿幾乎一律會用來做為使用者特定動作的一次性回應，例如按一下功能表上的 [ **貼** 上]。 雖然 DDE 也可以由使用者起始，但它通常會在沒有使用者進一步介入的情況下繼續進行。

動態資料交換 Management Library (DDEML) 提供可簡化將 DDE 功能新增至應用程式之工作的介面。 應用程式會使用 DDEML 所提供的函式來管理 DDE 交談，而不是直接傳送、張貼和處理 DDE 訊息。 DDE 交談是用戶端與伺服器應用程式之間的互動。 DDEML 也提供一種方法來管理在 DDE 應用程式之間共用的字串和資料。 DDE 應用程式不會使用原子和指向共用記憶體物件的指標，而是會建立和交換字串控制碼，以識別用來識別 DDE 物件的字串和資料控制碼。 DDEML 提供的函式 ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) ，可讓伺服器應用程式註冊它所支援的服務名稱。 接著，服務名稱會廣播到系統中的其他應用程式，而該應用程式會使用名稱連接到伺服器。 DDEML 也可確保 DDE 應用程式之間的相容性，方法是要求這些應用程式以一致的方式執行 DDE 通訊協定。

使用以訊息為基礎之 DDE 通訊協定的現有應用程式與使用 DDEML 的應用程式完全相容;也就是說，使用訊息型 DDE 的應用程式可以使用 DDEML 來建立交談，以及與應用程式執行交易。 除了在新的應用程式中使用 DDE 訊息，您還可利用 DDEML 以及它所提供的許多增強功能。

若要使用 DDEML，您必須包含 DDEML。H 標頭檔的原始程式檔中，與 USER32 連結。LIB 檔案，並確定 DDEML.DLL 檔案位於系統的路徑中。

每當 DDEML 函式失敗時，應用程式就可以呼叫 [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) 函數來判斷失敗的原因。 **DdeGetLastError** 會傳回錯誤值，以指定最新錯誤的原因。

 

 




