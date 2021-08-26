---
title: 同步作業
description: 當 RasDial 被叫用為同步作業時，除非已建立連接或發生錯誤，否則函數不會傳回。
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c923a22758e7d6b9563cde9e4c9b2ce6036afa47f85116c0c18ed523996e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025608"
---
# <a name="synchronous-operations"></a>同步作業

當 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 被叫用為同步作業時，除非已建立連接或發生錯誤，否則函數不會傳回。 同步模式提供了一種簡單的方法，讓 RAS 用戶端建立連接。 用戶端可以直接呼叫 **RasDial**、等候函式傳回，然後呼叫 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函數來判斷連接作業是否成功。 一旦建立連線之後，用戶端應用程式就可以在不中斷連接的情況下終止。 如果發生錯誤，用戶端應用程式必須在終止之前 [關閉連接](disconnecting.md) 作業。

同步模式的缺點是，用戶端在連接作業繼續時，不會收到進度通知。 這項缺少進度通知的因應措施是，同步模式用戶端可以使用呼叫 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 的個別執行緒來輪詢和顯示目前的狀態。 不過，對於想要接收進度資訊的 RAS 用戶端，慣用的技巧是以非同步方式叫用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 。

 

 




