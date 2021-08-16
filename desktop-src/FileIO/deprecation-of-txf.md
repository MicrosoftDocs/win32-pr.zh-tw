---
description: 本主題討論在一般使用案例中使用交易式 NTFS API (TxF) 的替代方案。
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: 使用交易式 NTFS 的替代方案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765968"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>使用交易式 NTFS 的替代方案

-   [摘要](#abstract)
-   [簡介](#introduction)
-   [依案例的 TxF 替代方案](#alternatives-to-txf-by-scenario)
-   [使用「檔相似」資料更新單一檔案的應用程式](#applications-updating-a-single-file-with-document-like-data)
-   [對多個檔案和/或登錄 hive 執行更新的應用程式](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [管理一組結構化資料的應用程式](#applications-managing-a-set-of-structured-data)
-   [交易的應用程式牽涉到本機 NTFS 磁片區上的檔案和外部 SQL 資料庫中的資料表](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [關閉 & 建議的動作](/windows)

## <a name="abstract"></a>摘要

Microsoft 強烈建議開發人員調查使用討論的替代方案 (或在某些情況下，調查其他替代) ，而不是採用可能無法在未來版本的 Windows 中使用的 API 平臺。

## <a name="introduction"></a>簡介

在 Windows Vista 中引進了 TxF，作為將不可部分完成的檔案交易引入 Windows 的途徑。 它可讓 Windows 開發人員在交易中使用單一檔案、在涉及多個檔案的交易中，以及橫跨多個來源的交易（例如，透過 TxR) 的登錄 (和資料庫 (，例如 SQL) ），擁有交易式不可部分完成的檔案作業。 雖然 TxF 是一組強大的 api，但在此 api 平臺中，開發人員對開發人員而言有很大的興趣，因為 Windows Vista 主要是因為它的複雜性和各種不同的細微之處，而開發人員必須在應用程式開發過程中考慮 如此一來，Microsoft 會考慮在未來版本的 Windows 中淘汰 TxF api，以專注于其他功能和 api 的開發和維護工作，這些功能和 api 對於較大的大部分客戶都有更大的價值。 下一節將說明可讓您以 TxF 針對數種應用程式案例類型達成類似結果的範例替代方法。

## <a name="alternatives-to-txf-by-scenario"></a>依案例的 TxF 替代方案

有了上述限制，開發人員應該調查 TxF 的替代方案，以涵蓋 TxF 不符合的應用程式案例。 此處所討論的一些建議，是為了讓開發人員可以考慮使用 TxF 的一般 TxF。 請注意，這份清單並不完整，也不會完成。

## <a name="applications-updating-a-single-file-with-document-like-data"></a>使用「檔相似」資料更新單一檔案的應用程式

許多應用程式會處理「類似檔」的資料，通常會將整份檔載入記憶體中、操作它，然後寫回以儲存變更。 此處所需要的不可部分完成性，是完全套用或未套用的變更，因為不一致的狀態會導致檔案損毀。 常見的方法是將檔寫入至新的檔案，然後以新的檔案取代原始檔案。 其中一個方法是使用 [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) API。

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>對多個檔案和/或登錄 hive 執行更新的應用程式

有許多應用程式都需要以不可部分完成的方式，對一組檔案和登錄進行更新。 此案例最常透過安裝程式應用程式來達成，例如 Windows Installer。 如需 Windows Installer 的詳細資訊，請參閱[Windows Installer](/windows/desktop/Msi/windows-installer-portal)。

## <a name="applications-managing-a-set-of-structured-data"></a>管理一組結構化資料的應用程式

許多應用程式會管理一組不同類型的專屬資料結構，作為儲存資料的方式。 如果在更新作業期間發生失敗，則這些應用程式的重大挑戰就是維護內部指標/參考完整性的流程。 為此建立機制的確是「困難的問題」，因此大部分的應用程式都會依賴真正的資料庫伺服器來管理其資料集。

有兩個協助管理結構化資料的建議如下：

-   Microsoft 會在 Windows 中提供可擴充的儲存體引擎 (ESE) 收件匣，讓應用程式能夠執行交易資料更新和抓取作業。 如需可延伸的儲存體引擎 (ESE) 的詳細資訊，請參閱 <https://msdn.microsoft.com/library/gg269259.aspx> 。
-   對於需要更強大、穩定且可擴充之資料庫提供者的應用程式，建議客戶考慮使用 Microsoft SQL Server 提供的 Filestream 功能。 如需 SQL filestream 的詳細資訊，請參閱 <https://technet.microsoft.com/library/bb933993.aspx> 。

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>交易的應用程式牽涉到本機 NTFS 磁片區上的檔案和外部 SQL 資料庫中的資料表

有大型資料集需要的應用程式類別，或需要在涉及外部資料庫和本機儲存體的作業中具有交易不可部分完成性。 在此案例中，強烈建議開發人員考慮使用 SQL filestream 來執行交易式檔案作業。 如需 SQL filestream 的詳細資訊，請參閱 <https://technet.microsoft.com/library/bb933993.aspx> 。

## <a name="closing--recommended-action"></a>關閉 & 建議的動作

TxF 是一組複雜且差別細微的 Api，不常用於協力廠商應用程式。 由於這些 api 在未來的 Windows 版本中可能無法使用，而且有更簡單的替代方法可達成許多針對 txf 開發的案例，因此 Microsoft 強烈建議開發人員調查這些替代方法，而不是在其應用程式中建立 txf 的相依性。

 

 
