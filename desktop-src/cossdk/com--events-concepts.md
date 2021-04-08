---
description: COM + 事件概念
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: COM + 事件概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689220"
---
# <a name="com-events-concepts"></a>COM + 事件概念

COM + 事件服務是一個自動、 *鬆散結合的事件* 系統，可將來自不同發行者的事件資訊儲存在 com + 目錄中。 訂閱者可以查詢此事件存放區，並選取想要聽取的事件。

> [!Note]  
> *事件* 是由 com + 介面中的方法所識別（稱為 *事件方法*），並由發行者發出，並透過 com + 事件服務分派給正確的訂閱者或訂閱者。 事件方法必須是唯一的名稱，而且只能包含輸入參數 (沒有任何輸出或輸入/輸出參數) 。 傳回值必須是 **HRESULT**。

 

COM + 事件服務會處理發行者和訂閱者的大部分事件語義。 發行者會提供發佈事件種類和訂閱者要求發行者的事件種類。 不同于 *緊密結合的事件* 系統（發行者必須直接處理呼叫訂閱者的額外負荷），com + 事件服務會維護 com + 目錄中的訂閱資料，而不受發行者和訂閱者的影響。 這會簡化發行者和訂閱者的程式設計模型，因為 COM + 訂閱者元件不需要包含建立訂閱的邏輯。

由於 COM + 事件訂閱資料的生命週期與「發行者」或「訂閱者」的存留期不同，因此可以在「訂閱者」或「發行者」應用程式為作用中之前建立訂閱。 這也表示可以另外開發和部署發行者和訂閱者。 您可以撰寫發行者，而不知道訂閱者的數目和位置。 訂閱者會使用 COM + 事件服務來尋找發行者及管理其訂閱。

本章節中的下列主題提供有關 COM + 事件服務核心元素的詳細資訊，以及如何使用這些專案。

-   [COM + 事件類別物件](the-com--event-class-object.md)
-   [訂用帳戶](subscriptions.md)
-   [在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
-   [在 COM + 中篩選事件](filtering-events-in-com-.md)
-   [使用 com + 事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 事件安全性考慮](com--events-security-considerations.md)
</dt> <dt>

[COM + 事件工作](com--events-tasks.md)
</dt> </dl>

 

 



