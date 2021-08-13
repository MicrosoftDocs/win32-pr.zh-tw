---
description: 系統管理員可以強制 COM 用戶端應用程式一律使用現有封裝中的相同 COM 伺服器複本&\# 郵件，而不會影響其他應用程式&\# 郵件; 方法是指定 COM 伺服器和用戶端之間的隔離元件關聯性。
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: 使現有封裝中的 COM 元件成為私用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5119e2d9417f51bb815fe9c76cd47be496e4c03cab81e4e0ccd2b7c49c7b8b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629029"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>使現有封裝中的 COM 元件成為私用

系統管理員可以藉由指定 COM 伺服器和用戶端之間的 [隔離元件](isolated-components.md) 關聯性，強制 com 用戶端應用程式一律使用現有封裝中的相同 com 伺服器複本，而不會影響其他應用程式。 這會將 COM 伺服器元件的私用複本安裝至用戶端應用程式專用的位置。 系統管理員必須使用轉換或封裝撰寫工具來執行下列作業：

-   將 COM 伺服器 DLL 和 .exe 用戶端放在不同的元件中。
-   在 [元件共用] 資料行中，以 COM-用戶端元件的 [IsolatedComponent 資料表](isolatedcomponent-table.md) 輸入記錄 \_ ，並在 [元件應用程式] 資料行中輸入用戶端應用程式 \_ 。 在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。
-   在元件 [資料表](component-table.md)記錄中，為共用的元件設定 **msidbComponentAttributesSharedDllRefCount** 位 \_ 。 在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。

 

 



