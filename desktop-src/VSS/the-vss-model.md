---
description: VSS 的設計目的是要解決一般磁片區備份問題中所述的問題。
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: VSS 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970431"
---
# <a name="the-vss-model"></a>VSS 模型

VSS 的設計目的是要解決 [一般磁片區備份問題](common-volume-backup-issues.md)中所述的問題。

VSS 模型包含下列各項：

-   陰影複製機制。 VSS 提供磁片的快速磁片區狀態快速捕獲，也就是磁片區的 [*陰影複製*](vssgloss-s.md) 。 此磁片區複本與即時磁片區並存存在，而且會包含磁片上所有檔案的複本，這些檔案會以個別裝置的形式有效儲存和提供。
-   透過應用程式協調進行一致的檔案狀態。 VSS 提供以 COM 為基礎的事件驅動處理序間通訊機制，參與的進程可以用來判斷有關備份、還原和陰影複製 (磁片區捕獲) 作業的系統狀態。 這些事件會定義應用程式用來修改磁片 ([*寫入*](vssgloss-w.md) 器上資料的階段，) 可以在建立陰影複製之前，將所有的檔案帶入一致的狀態。
-   將應用程式停機時間降到最低。 VSS 陰影複製會與要備份之磁片區的即時複本並行存在，因此除了陰影複製準備和建立的短暫期間，應用程式可以繼續其工作。 實際建立陰影複製所需的時間（在 [*凍結*](vssgloss-f.md) 和 [*解除凍結*](vssgloss-t.md) 事件之間發生）通常需要大約一分鐘的時間。

    當寫入器準備進行陰影複製時，包括排清 i/o 和儲存狀態 (請參閱) [的備份前工作總覽](overview-of-pre-backup-tasks.md) 重要，它比實際備份磁片區所需的時間短一點，因為大型磁片區可能需要數小時的時間。

-   VSS 的整合介面。 VSS 會將陰影複製機制抽象化在通用介面內，同時讓硬體廠商新增及管理其專屬提供者的獨特功能。 任何備份應用程式 [*(要求*](vssgloss-r.md) 者) 和任何寫入器都應該能夠在支援 VSS 介面的任何磁片儲存系統上執行。
-   Multivolume 備份。 VSS 支援 [*陰影複製集*](vssgloss-s.md)（這是陰影複製的集合），跨多個廠商的多個磁片區類型。 陰影複製集中的所有陰影複製都將使用相同的時間戳記來建立，並且會呈現 multivolume 磁片狀態的相同磁片狀態。
-   原生陰影複製支援。 從 Windows XP 開始，陰影複製支援可透過 VSS 提供，做為 Windows 作業系統的原生部分。 只要系統上至少有一個 NTFS 磁片，就可以將這些系統設定為支援所有掛接之磁片系統的陰影複製。

 

 



