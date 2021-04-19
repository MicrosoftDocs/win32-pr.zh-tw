---
description: 使用交易式 NTFS 來維護資料完整性。
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: 使用交易式 NTFS 的時機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989472"
---
# <a name="when-to-use-transactional-ntfs"></a>使用交易式 NTFS 的時機

應用程式可以使用交易式 NTFS (TxF) 在非預期的錯誤情況期間，保留磁片上資料的完整性。 一般情況下，應用程式應該考慮使用 TxF （如果應用程式正在清除檔案，以及使用其他技術來維持資料完整性）。 TxF 可以更妥善地執行並簡化應用程式的錯誤處理常式代碼，同時改善錯誤的復原和可靠性。 本主題中的下列各節提供使用 TxF 的案例範例。

## <a name="updating-a-file"></a>更新檔案

檔案的更新是常見且一般簡單的操作。 但是，如果在應用程式更新磁片上的資訊時，系統或應用程式失敗，結果可能會造成嚴重的後果，因為使用者資料可能會因已部分完成的檔案更新作業而損毀。 健全的應用程式通常會執行一系列的檔案複製和檔案重新命名，以確保在系統失敗時資料不會損毀。

TxF 讓應用程式可以輕鬆地保護檔案更新作業，避免系統或應用程式失敗。 為了安全地更新檔案，應用程式會以交易模式開啟檔案、進行必要的更新，然後認可交易。 如果在檔案更新期間，系統或應用程式失敗，則 TxF 會自動將檔案還原至檔案更新開始之前的狀態，這樣可避免檔案損毀。

## <a name="multi-file-updates"></a>多檔案更新

當單一邏輯作業影響多個檔案時，TxF 更為重要。 例如，如果您想要使用工具來重新命名網站上的其中一個 HTML 或 ASP 頁面，設計完善的工具也會修正所有連結，以使用新的檔案名。 不過，在此作業期間發生失敗時，網站會處於不一致的狀態，而某些連結仍會參考舊的檔案名。 藉由讓檔案重新命名作業和連結修正作業成為單一交易，TxF 可確保檔案重新命名和連結修正成功或失敗，以做為單一作業。

## <a name="consistent-concurrent-updates"></a>一致的並行更新

TxF 會隔離並行交易。 如果應用程式在另一個應用程式開啟交易式更新的相同檔案時，開啟交易式讀取的檔案，則 TxF 會將這兩個交易的效果彼此隔離。 換句話說，交易式讀取器一律會查看單一的一致版本檔案，即使該檔案正在由另一個交易進行更新。

應用程式可以使用這種功能，讓客戶在其他客戶進行更新時查看檔案。 例如，交易式 web 伺服器可以提供單一且一致的檔案視圖，而另一個工具會同時更新這些檔案。

> [!Note]  
> 在不同的交易中，TxF 不支援多個寫入器的並行更新。 TxF 僅支援具有多個並行和一致讀取器的單一寫入器。

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>與其他交易的資源管理員協調

交易式檔案系統所使用的交易也可以搭配交易登錄使用。 檔案和登錄的更新會與單一交易協調。

藉由使用 [分散式交易協調器](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) 交易或系統交易，對 SQL、MSMQ 和其他交易式資源所做的更新，可以與交易檔案更新協調。 如需詳細資訊，請參閱 DTC 的 [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))。

## <a name="unsupported-scenarios"></a>不支援的案例

TxF 不支援下列交易案例：

-   網路磁片區上的交易，例如檔案共用。 CIFS/SMB 通訊協定不支援 TxF。
-   NTFS 以外的任何檔案系統上的交易。
-   針對由用戶端快取快取的檔案進行的交易作業。
-   使用物件識別碼存取檔案。
-   任何共用的寫入器案例。
-   任何情況下，檔案會在一段時間內開啟一段很長的時間)  (天或數周。

 

 
