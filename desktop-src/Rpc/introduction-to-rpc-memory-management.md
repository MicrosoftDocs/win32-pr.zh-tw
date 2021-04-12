---
title: RPC 記憶體管理簡介
description: " (RPC) 記憶體管理的遠端程序呼叫簡介。"
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316063"
---
# <a name="introduction-to-rpc-memory-management"></a>RPC 記憶體管理簡介

在 RPC 的內容中，記憶體管理牽涉到：

-   在用戶端和伺服器執行緒的不同位址空間中，為用戶端與伺服器之間的單一概念位址空間，配置和解除配置所需的記憶體。
-   判斷哪個軟體元件負責管理記憶體—應用程式或 MIDL 產生的存根。
-   選取會影響記憶體管理的 MIDL 屬性：方向屬性、指標屬性、陣列屬性，以及 ACF 屬性的 \[ [位元組 \_ 計數](/windows/desktop/Midl/byte-count) \] 、 \[ [配置](/windows/desktop/Midl/allocate) \] 和 \[ [啟用 \_ 配置](/windows/desktop/Midl/enable-allocate) \] 。

當程式在其位址空間中呼叫函式或程式時，記憶體管理會比在分散式應用程式中更直接。 為了說明，下圖描述二進位樹狀結構。 為了將此資料結構傳遞至其位址空間中的程式，程式只會將指標傳遞至樹狀結構的根。

![二進位樹狀結構，其中包含指向樹狀結構根目錄之資料的指標](images/bintree.png)

用戶端/伺服器 RPC 應用程式會在兩個不同的記憶體空間之間共用資料。 這些記憶體空間不一定會在同一部電腦上。 無論何種方式，用戶端和伺服器都無法直接存取彼此的記憶體空間。 RPC 取決於在伺服器程式的位址空間中模擬用戶端程式位址空間的能力。 它也必須從伺服器傳回用戶端記憶體中的資料，包括新的和變更的資料。

在上圖所示的二進位樹狀結構中，將根節點的指標傳遞至遠端程式並不足夠。 程式或存根必須將整個樹狀結構傳遞到伺服器的位址空間，才能讓遠端程式進行操作。

 

 