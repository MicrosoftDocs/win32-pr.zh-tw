---
description: 在 Windows 通訊端中 Pseudoblocking 虛擬封鎖作業 (Winsock) 。
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: 虛擬封鎖和真正封鎖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989315"
---
# <a name="pseudo-blocking-and-true-blocking"></a>虛擬封鎖和真正封鎖

在16個 Windows 環境中，作業系統不支援真正的封鎖;因此，無法立即完成的封鎖作業會依照下列方式處理：

-   服務提供者會起始作業，然後輸入迴圈，在這種情況下，它會分派任何 Windows 訊息 (將處理器產生到另一個執行緒（如有需要）) 
-   然後，它會檢查 Windows 通訊端函式是否完成。
-   如果函式已完成，或已叫用 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，迴圈就會終止，而且封鎖函式會以適當的結果完成。

這是「虛擬封鎖」一詞所指的，而上述的迴圈稱為預設封鎖攔截。

 

 
