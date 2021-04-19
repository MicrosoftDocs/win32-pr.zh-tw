---
description: 系統管理員可以強制用戶端應用程式一律使用現有封裝中的相同非 COM 伺服器複本&\# 郵件，而不會影響其他應用程式&\# 郵件; 方法是指定伺服器與用戶端之間的隔離元件關聯性。
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: 將現有封裝中的非 COM 元件設為私用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972265"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>將現有封裝中的非 COM 元件設為私用

系統管理員可以藉由指定伺服器與用戶端之間的 [隔離元件](isolated-components.md) 關聯性，來強制用戶端應用程式一律使用現有封裝中的相同非 COM 伺服器複本，而不會影響其他應用程式。 這會將伺服器元件的私用複本安裝至用戶端應用程式專用的位置。 系統管理員必須使用轉換或封裝撰寫工具來執行下列作業：

-   將伺服器 DLL 和 .exe 用戶端放在不同的元件中。
-   在 [元件共用] [](isolatedcomponent-table.md)資料行中的用戶端元件和 [ \_ 元件應用程式] 資料行中的用戶端應用程式中，輸入 IsolatedComponent 資料表中的記錄 \_ 。 在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。
-   在元件 [資料表](component-table.md)記錄中，為共用的元件設定 **msidbComponentAttributesSharedDllRefCount** 位 \_ 。 在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。

 

 



