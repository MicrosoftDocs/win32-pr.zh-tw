---
title: 系結控制碼
description: 系結是在用戶端程式和伺服器程式之間建立邏輯連接的程式。 在用戶端與伺服器之間撰寫系結的資訊是由稱為系結控制碼的結構所表示。
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932338"
---
# <a name="binding-handles"></a>系結控制碼

系結是在用戶端程式和伺服器程式之間建立邏輯連接的程式。 在用戶端與伺服器之間撰寫系結的資訊是由稱為系結控制碼的結構所表示。

系結控制碼類似于 fopen C 執行時間程式庫函式傳回的檔案控制代碼，或是函式 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 傳回的視窗控制碼。

如同這些控制碼，您的應用程式無法直接存取及操作系結控制碼中的資訊。 系結控制碼資料結構中的資訊僅適用于 RPC 執行時間程式庫。 您可以提供控制碼、執行時間程式庫存取和操作適當的資料。

本節提供下列主題中系結控制碼的討論：

-   [系結控制碼的類型](types-of-binding-handles.md)
-   [用戶端系結](client-side-binding.md)
-   [伺服器端系結](server-side-binding.md)
-   [完整且部分系結的控制碼](fully-and-partially-bound-handles.md)
-   [解讀系結資訊](interpreting-binding-information.md)
-   [Microsoft RPC Binding-Handle 擴充功能](microsoft-rpc-binding-handle-extensions.md)
-   [Binding 處理函式](binding-handle-functions.md)
-   [RPC 名稱服務資料庫](the-rpc-name-service-database.md)

 

 