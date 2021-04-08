---
description: 除非您呼叫 MsiDatabaseCommit，否則對安裝資料庫所做的變更不會寫入至資料庫。
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: 認可資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850608"
---
# <a name="committing-databases"></a><span data-ttu-id="2e242-103">認可資料庫</span><span class="sxs-lookup"><span data-stu-id="2e242-103">Committing Databases</span></span>

<span data-ttu-id="2e242-104">除非您呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，否則對安裝資料庫所做的變更不會寫入至資料庫。</span><span class="sxs-lookup"><span data-stu-id="2e242-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="2e242-105">**若要確保資料庫中所做的變更已完成**</span><span class="sxs-lookup"><span data-stu-id="2e242-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="2e242-106">當您呼叫 [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)來呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)時，請檢查是否會寫入資料表。</span><span class="sxs-lookup"><span data-stu-id="2e242-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="2e242-107">呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) 函數來完成資料庫的變更。</span><span class="sxs-lookup"><span data-stu-id="2e242-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="2e242-108">在資料庫中進行的變更會累積，而且在您呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)之前，不會反映在實際的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="2e242-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="2e242-109">暫存資料行或資料列不會認可至資料庫。</span><span class="sxs-lookup"><span data-stu-id="2e242-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="2e242-110">當資料庫關閉時，自上次 **MsiDatabaseCommit** 之後所做的所有變更都會自動回復。</span><span class="sxs-lookup"><span data-stu-id="2e242-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



