---
description: 在 Windows Vista 和 Windows Server 2008 中，使用者資料和系統資料的預設位置已變更。
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: 連接點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980803"
---
# <a name="junction-points"></a>連接點

在 Windows Vista 和 Windows Server 2008 中，使用者資料和系統資料的預設位置已變更。 例如，先前儲存在% SystemDrive% Documents and Settings 目錄中的使用者資料， \\ 現在會儲存在% SystemDrive% \\ Users 目錄中。 為了回溯相容性，舊的位置具有指向新位置的連接點。 例如，C： \\ Documents 和 Settings 現在是指向 C： Users 的連接點 \\ 。 備份應用程式必須能夠備份和還原連接點。

這些連接點可識別如下：

-   它們具有檔 \_ 屬性重新 \_ 分析 \_ 點、檔 \_ 屬性 \_ 隱藏，以及檔 \_ 屬性 \_ 系統檔案屬性設定。
-   它們也有 (Acl 的存取控制清單) 設定為拒絕所有人的讀取權限。

如果應用程式有必要的許可權，則呼叫特定路徑的應用程式可以跨越這些連接點。 不過，嘗試列舉連接點的內容將會導致失敗。 備份應用程式不會跨越這些連接點，或嘗試在其下備份資料，原因有兩個：

-   這樣做可能會導致備份應用程式多次備份相同的資料。
-   它也可能會導致迴圈參考)  (迴圈。

## <a name="per-user-junctions-and-system-junctions"></a>Per-User 接合和系統接合

在 Windows Vista 和 Windows Server 2008 中用來提供檔案和登錄虛擬化的連接點可以分為兩個類別：每個使用者的連接和系統連接。

每個使用者的連接都會建立在每個個別使用者的設定檔內，以提供使用者應用程式的回溯相容性。 位於 C： \\ users 使用者名稱的連接點 \\  \\ 我的檔指向 C： \\ 使用者使用者 \\ *名稱* \\ 檔是每個使用者的連接點範例。 建立使用者設定檔時，設定檔服務會建立每位使用者的連接。

其他連接是不位於使用者使用者名稱目錄下的系統連接 \\  。 系統接合的範例包括：

-   檔和設定
-   所有使用者、公用和預設使用者設定檔中的連接

系統連接是由 Windows 歡迎使用 (（也稱為「電腦現成體驗」或 mOOBE) ）所叫用的 userenv.dll 所建立。

> [!Note]  
> 如果使用者將系統語言變更為英文以外的語言，則會以當地語系化名稱建立每位使用者和系統連接點。

 

 

 



