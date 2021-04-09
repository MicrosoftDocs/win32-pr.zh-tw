---
title: 復原檔案系統
description: 復原檔案系統
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104024271"
---
# <a name="resilient-file-system"></a>復原檔案系統

## <a name="platform"></a>平台

**伺服器** – Windows Server 2012 

## <a name="description"></a>Description

復原檔案系統 (ReFS) 是新的本機檔案系統。 它可將資料的可用性最大化，儘管過去發生的錯誤會造成資料遺失或停機。 資料完整性可確保商務關鍵資料受到保護，避免發生錯誤並可在需要時使用。 其架構的設計目的是為了在不斷成長的資料集大小和動態工作負載的時代提供可調整性和效能。

ReFS 的主要功能如下：

-   **完整性**： ReFS 會儲存資料，以防止許多可能導致資料遺失的常見錯誤。 檔案系統中繼資料一律受到保護。 （選擇性）您可以針對每個磁片區、每個目錄或每個檔案來保護使用者資料。 如果發生損毀，ReFS 可以偵測到，當設定儲存空間時，會自動校正損毀。 發生系統錯誤時，ReFS 的設計是為了快速從該錯誤復原，而不會遺失使用者資料。
-   **可用性**： ReFS 的設計目的是要排定資料的可用性。 使用 ReFS 時，如果發生損毀，而且無法自動修復，線上搶救程式就會當地語系化為損毀區域，而且不需要任何磁片區停機時間。 簡言之，如果發生損毀，ReFS 將保持連線。
-   擴充 **性**： ReFS 是針對目前的資料集大小和明天的資料集大小所設計。它已針對高擴充性優化。
-   **應用程式相容性**：若要最大化 AppCompat，REFS 支援 NTFS 功能的子集，以及廣泛採用的 Win32 api。
-   **主動式錯誤識別**： ReFS 的完整性功能是透過資料完整性掃描器來利用 (「清除程式」 ) 會定期掃描磁片區、嘗試找出潛在損毀，然後主動觸發修復損毀的資料。

## <a name="resources"></a>資源

-   [建立 Windows 8 的 Blog 文章–為 Windows 建立新一代的檔案系統： ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [應用程式相容性和 ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 