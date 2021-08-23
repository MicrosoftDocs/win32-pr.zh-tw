---
title: 通知的運作方式
description: 通知的運作方式
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756368"
---
# <a name="how-notifications-work"></a>通知的運作方式

通知是源自物件應用程式，並透過物件處理常式流向容器。 如果物件是連結化物件，則連結化物件會從物件處理常式攔截通知，並直接通知容器。

物件應用程式必須管理註冊要求，並追蹤傳送通知的位置，並在適當時傳送這些通知。 OLE 提供兩個元件物件來簡化這項工作：複合檔案通知的 OleAdviseHolder 和資料通知的 DataAdviseHolder。

物件應用程式會決定提示傳送每個特定通知的條件，以及每個通知的傳送頻率。 當它適用于傳送多個通知時，會先傳送哪個通知，不重要。可以依任何順序傳送。

通知的時間會影響物件應用程式及其容器之間的效能和協調。 雖然通知傳送太頻繁，但傳送的通知太過頻繁，導致同步處理中的容器無法執行。 通知頻率可以與應用程式重新繪製的速率進行比較。 因此，使用類似的邏輯來執行通知的時機 (如同用於重新繪製) 是明智的做法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[通知](notifications.md)
</dt> </dl>

 

 