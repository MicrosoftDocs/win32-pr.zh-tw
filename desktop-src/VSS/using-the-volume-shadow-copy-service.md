---
description: VSS 備份和還原作業各自都會使用通訊協定來與使用大型儲存體 (寫入器) 的系統互動，以及 (要求者) 進行備份。
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: 使用磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866248"
---
# <a name="using-the-volume-shadow-copy-service"></a>使用磁碟區陰影複製服務

VSS 備份和還原作業各自都會使用通訊協定來與使用大型儲存體 (寫入器) 的系統互動，以及 (要求者) 進行備份。

備份和還原作業主要是由要求者驅動，藉由產生可供寫入器處理的全系統 COM 事件，來控制寫入器和提供者的行為。 因為事件產生的方法是非同步，所以寫入器對要求者的狀態有有限的控制權，可透過 VSS 取得的非同步處理常式 (查看 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)) 。

這項互動需要基本的資料結構，描述檔案和檔案群組 ([*元件*](vssgloss-c.md)) ，以及元資料模型，以允許儲存備份資訊和允許寫入器/要求者通訊。

-   [VSS 應用程式相容性](usage-conventions.md)
-   [設定 VSS](configuring-vss.md)
-   [VSS 中繼資料](vss-metadata.md)
-   [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)
-   [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)
-   [在 VSS 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)

 

 



