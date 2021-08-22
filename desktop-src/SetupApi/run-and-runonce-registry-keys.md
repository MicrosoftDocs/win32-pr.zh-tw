---
description: Run 和 RunOnce 登錄機碼會導致每次使用者登入時都會執行程式。
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: 執行和 RunOnce 登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665238"
---
# <a name="run-and-runonce-registry-keys"></a>執行和 RunOnce 登錄機碼

Run 和 RunOnce 登錄機碼會導致每次使用者登入時都會執行程式。 索引鍵的資料值是不超過260個字元的命令列。 藉由新增表單 *描述* - *字串* = *命令列* 的專案來註冊要執行的程式。 您可以在機碼下撰寫多個專案。 如果有一個以上的程式在任何特定的金鑰下註冊，這些程式執行的順序就會不定。

Windows 登錄包含下列四個執行和 RunOnce 索引鍵：

-   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

根據預設，在執行命令列之前，會刪除 RunOnce 索引鍵的值。 您可以在 RunOnce 值名稱前面加上驚嘆號 (！ ) 來延遲刪除值，直到命令執行為止。 如果沒有驚嘆號前置詞，則當您下次啟動電腦時，將不會要求關聯的程式執行。

根據預設，在保管庫模式下啟動電腦時，會忽略這些機碼。 RunOnce 索引鍵的值名稱可以加上星號 (\*) 來強制程式即使在保管庫模式下也可以執行。

從這些機碼執行的程式不應該在執行期間寫入金鑰，因為這會干擾在機碼下註冊的其他程式的執行。 應用程式應該只針對暫時性狀況使用 RunOnce 索引鍵，例如完成應用程式設定。 應用程式不能持續在 RunOnce 下重建專案，因為這會干擾 Windows 安裝程式。
