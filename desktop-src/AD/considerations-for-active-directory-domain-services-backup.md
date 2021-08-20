---
title: Active Directory Domain Services 備份的考慮
description: 目錄服務資料可以複寫。 還原前必須先建立復原方案。
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory，復原規劃
- Active Directory Domain Services Active Directory，備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61fbe30d6c8e74a0896fe1b8b9d6ed34bf9caae2f37fc2ac7de2afd8a75c00c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022012"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Active Directory Domain Services 備份的考慮

目錄服務資料可以複寫。 還原前必須先建立復原方案。 其中一個選項是還原目錄的複本，然後傳播從網域中的其他複本備份之後發生的變更。

在某些情況下，您可能會想讓還原的複本優先于網域中的其他複本。 例如，如果意外刪除物件，並將刪除複寫到所有網域控制站，您就可以從刪除物件之前所做的備份還原一個複本來還原物件。 然後您會使用 NTDSUtil 公用程式，將還原的物件標示為已授權還原。 還原的物件接著會複寫到其他 Dc，而還原的複本將會收到自從進行備份以來發生的所有其他物件的更新。 所有複本的最終結果與還原前的結果相同，不同之處在于，已不會再刪除授權還原的物件。

備份期間發生的所有變更都會儲存在暫存記錄檔中，並在備份完成時新增到備份組的結尾。

任何復原方案都應該確保備份的存留期不應超過 Active Directory 的標記存留期。 如需標記存留期的詳細資訊，請參閱 TechNet 主題- [管理 Active Directory 備份和](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10))復原的簡介。 還原超過標記存留期的備份，可能會導致還原的網域控制站擁有不會在其他 Dc 上複寫的物件。 如果在進行備份之後刪除物件，並且在永久移除已刪除物件的標記之後進行還原，就會發生這種情況。 還原的 DC 在刪除之前會有物件存在，而其他 Dc 則沒有該物件曾經存在的記錄。 在此情況下，系統管理員必須手動刪除已還原之網域控制站上的每個非複寫物件。

不支援 Active Directory Domain Services 的增量備份;需要完整備份。

 

 