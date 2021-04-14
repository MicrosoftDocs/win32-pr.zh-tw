---
title: '架構 (文字服務架構) '
description: 架構
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- 文字服務架構 (TSF) ，架構
- TSF (文字服務架構) ，架構
- 文字服務，架構
- 啟用 TSF 的應用程式，架構
- 文字服務架構 (TSF) 、元件
- TSF (文字服務架構) 、元件
- 文字服務，元件
- 啟用 TSF 的應用程式，元件
- 文字服務架構 (TSF) 、應用程式
- TSF (文字服務架構) 、應用程式
- 文字服務，應用程式
- 啟用 TSF 的應用程式，關於
- 文字服務架構 (TSF) 、文字服務
- TSF (文字服務架構) 、文字服務
- 文字服務，關於
- 啟用 TSF 的應用程式，文字服務
- 文字服務架構 (TSF) 、TSF manager
- TSF (文字服務架構) ，TSF 管理員
- 文字服務，TSF 管理員
- 啟用 TSF 的應用程式，TSF 管理員
- TSF 管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555606"
---
# <a name="architecture-text-services-framework"></a>架構 (文字服務架構) 

文字服務架構包含三個主要元件：

-   **應用程式：** 應用程式作業通常包括顯示、直接編輯和儲存文字。 應用程式會藉由執行支援特定介面的 COM 伺服器，並使用 TSF 管理員公開的介面，與 TSF 通訊，藉此提供文字的存取。 在此檔中，「應用程式」一詞指的是啟用 TSF 的應用程式，除非另有指定。
-   **文字服務：** 文字服務可做為應用程式的文字提供者。 文字服務可以取得應用程式的文字，並將文字寫入至應用程式。 文字服務也可以將資料和屬性與文字區塊產生關聯。 文字服務會實作為用來向 TSF 註冊本身的 COM 內部進程伺服器。 註冊之後，使用者會使用語言列或鍵盤快速鍵與文字服務互動。 可以安裝多個文字服務。
-   **TSF 管理員：** TSF manager 可作為應用程式與一或多個文字服務之間的中繼程式。 文字服務永遠不會直接與應用程式互動。 所有通訊都會通過 TSF 管理員。 TSF manager 是由作業系統所執行，而且無法取代。 在本檔中，除非另有指定，否則「管理員」一詞是指「TSF 管理員」。

下圖顯示 TSF 的主要架構元素。

![文字服務架構的架構](images/tsf-arch.gif)

使用此架構時，TSF 管理員會在應用程式和文字服務之間提供抽象層。 此抽象層可讓應用程式和一或多個文字服務共用文字，並且可讓 TSF 管理員管理文字服務。

 

 




