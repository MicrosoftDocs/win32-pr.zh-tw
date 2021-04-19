---
description: 備份和還原作業通常會將磁片上指定的預設位置中的檔案複製到備份媒體，然後從該媒體還原至磁片上的相同預設位置。
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: 非預設備份和還原位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989939"
---
# <a name="non-default-backup-and-restore-locations"></a>非預設備份和還原位置

備份和還原作業通常會將磁片上指定的預設位置中的檔案複製到備份媒體，然後從該媒體還原至磁片上的相同預設位置。

原因有很多，特別是在處理執行中的進程時，不是遵循這個簡單的模型。 VSS 支援使用非標準來源進行備份，並使用替代目的地進行還原，並包含使用檔案子集和重新對應檔案的機制。

-   [在備份期間使用替代路徑](working-with-alternate-paths-during-backup.md)
-   [在還原期間使用替代位置](working-with-alternate-locations-during-restore.md)
-   [在還原期間使用新目標](working-with-new-targets-during-restore.md)
-   [使用部分檔案](working-with-partial-files.md)
-   [使用導向的目標](working-with-directed-targets.md)

 

 



