---
description: 若要強制用戶端應用程式一律使用相同的非 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定伺服器與用戶端之間的隔離元件關聯性。
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: 將非 COM 元件安裝至私用位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852763"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>將非 COM 元件安裝至私用位置

若要強制用戶端應用程式一律使用相同的非 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定伺服器與用戶端之間的 [隔離元件](isolated-components.md) 關聯性。 這會將伺服器元件的私用複本安裝至用戶端應用程式專用的位置。 撰寫套件時，請執行下列動作：

-   將伺服器 DLL 和 .exe 用戶端放在不同的元件中。
-   在 [元件共用] [](isolatedcomponent-table.md)資料行中的用戶端元件和 [ \_ 元件應用程式] 資料行中的用戶端應用程式中，輸入 IsolatedComponent 資料表中的記錄 \_ 。 在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。
-   在元件 [資料表](component-table.md) 記錄中，為共用的元件設定 msidbComponentAttributesSharedDllRefCount 位 \_ 。 在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。
-   避免在元件之間撰寫共用的已註冊路徑。

 

 



