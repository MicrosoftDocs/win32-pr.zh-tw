---
description: 若要強制 COM 用戶端應用程式一律使用相同的 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定 COM 伺服器和用戶端之間的隔離元件關聯性。
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: 將 COM 元件安裝至私用位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848373"
---
# <a name="installing-a-com-component-to-a-private-location"></a>將 COM 元件安裝至私用位置

若要強制 COM 用戶端應用程式一律使用相同的 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定 COM 伺服器和用戶端之間的 [隔離元件](isolated-components.md) 關聯性。 這會將 COM 伺服器元件的私用複本安裝至用戶端應用程式專用的位置。 撰寫套件時，請執行下列動作：

-   將 COM 伺服器 DLL 和 .exe 用戶端放在不同的元件中。
-   在 [元件共用] 資料行中，以 COM-用戶端元件的 [IsolatedComponent 資料表](isolatedcomponent-table.md) 輸入記錄 \_ ，並在 [元件應用程式] 資料行中輸入用戶端應用程式 \_ 。 在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。
-   在元件 [資料表](component-table.md) 記錄中，為共用的元件設定 msidbComponentAttributesSharedDllRefCount 位 \_ 。 在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。

 

 



