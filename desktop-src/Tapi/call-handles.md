---
description: 如同會話識別碼總覽中所述，呼叫控制碼是 TAPI 2.2 應用程式用來識別特定通訊會話的方法。
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: 呼叫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de4c7eb6eb607e317a3291a186faea29bdc1ebfb3b54af6523591f94d402a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948112"
---
# <a name="call-handles"></a>呼叫控制碼

如同 [會話識別碼](./session-identifier-ovr.md) 總覽中所述，呼叫控制碼是 TAPI 2.2 應用程式用來識別特定通訊會話的方法。 當應用程式啟動會話時，TAPI 會傳回呼叫控制碼，以便在進一步的作業或查詢中使用。 當應用程式收到傳入會話的通知時，TAPI 也會在呼叫控制碼中傳遞。

當會話結束且會話狀態為閒置時，呼叫控制碼會維持有效，直到應用程式解除配置控制碼或關閉該行為止。 應用程式可能會關閉該行，或可能會收到 [**行 \_ 關閉**](line-close.md) 訊息。 如果行已關閉，則行呼叫的所有呼叫控制碼都會立即變成無效。

在呼叫還原為 *閒置* 狀態之後，仍允許應用程式讀取呼叫的資訊結構和狀態。 這可讓應用程式使用像是 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) 的作業來取得記錄用途的呼叫資訊。

當應用程式不再針對閒置呼叫的控制碼使用時，它必須呼叫 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 來釋放與呼叫相關的系統組態記憶體。 TAPI 會為每個具有呼叫控制碼的應用程式佈建記憶體。 服務提供者可能會配置記憶體來保存呼叫資訊。 解除配置應用程式的呼叫控制碼，可讓程式庫和服務提供者回收這些記憶體資源。 成功解除配置之後，應用程式在呼叫上的控制碼會變成 void。

應用程式本身必須釋放與它針對其本身所配置之呼叫相關的記憶體。

 

 
