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
# <a name="committing-databases"></a>認可資料庫

除非您呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，否則對安裝資料庫所做的變更不會寫入至資料庫。

**若要確保資料庫中所做的變更已完成**

1.  當您呼叫 [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)來呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)時，請檢查是否會寫入資料表。
2.  呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) 函數來完成資料庫的變更。

在資料庫中進行的變更會累積，而且在您呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)之前，不會反映在實際的資料庫中。 暫存資料行或資料列不會認可至資料庫。 當資料庫關閉時，自上次 **MsiDatabaseCommit** 之後所做的所有變更都會自動回復。

 

 



