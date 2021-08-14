---
description: Pseudoblocking Windows 通訊端中的虛擬封鎖作業 (Winsock) 。
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: 虛擬封鎖和真正封鎖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740940"
---
# <a name="pseudo-blocking-and-true-blocking"></a>虛擬封鎖和真正封鎖

在 16 Windows 環境中，作業系統不支援真正的封鎖;因此，無法立即完成的封鎖作業會依照下列方式處理：

-   服務提供者會起始作業，然後輸入迴圈，在這種情況下，它會分派任何 Windows 訊息， (視需要將處理器產生到另一個執行緒) 
-   然後，它會檢查 Windows 通訊端函數是否完成。
-   如果函式已完成，或已叫用 [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) ，迴圈就會終止，而且封鎖函式會以適當的結果完成。

這是「虛擬封鎖」一詞所指的，而上述的迴圈稱為預設封鎖攔截。

 

 
