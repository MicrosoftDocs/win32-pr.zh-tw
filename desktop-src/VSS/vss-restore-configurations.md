---
description: 執行中系統上的檔案還原可能會有問題。  (寫入器執行應用程式時，請務必) 指出還原期間發生問題時該怎麼做，例如，如果正在還原的檔案目前正在使用中。
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: VSS 還原設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48b3486128c6a91f601a89d697a4db9d8ab27fe9d3ac4cbef28dc870928d37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344195"
---
# <a name="vss-restore-configurations"></a>VSS 還原設定

執行中系統上的檔案還原可能會有問題。  (寫入器執行應用程式時，請務必) 指出還原期間發生問題時該怎麼做，例如，如果正在還原的檔案目前正在使用中。

在 VSS 下，寫入器有兩種互補的方式可管理還原：[*還原方法*](vssgloss-r.md) 和 [*還原目標*](vssgloss-r.md)。

此外，要求者可以選擇將檔案還原至先前未指定的位置，並通知寫入器 (參閱 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) 。

Restore 方法 (也會呼叫原始還原目標) 是由寫入器在備份時間指定的，並且會設定要用來還原未來所有元件之方法的全寫入器定義。 寫入器管理的所有檔案和元件都會共用相同的還原方法。

還原目標可讓寫入器變更在還原時還原特定元件的方式。 不同于 restore 方法，會為元件集定義還原目標。

您可以在下列主題中找到有關還原方法和還原目標使用方式的詳細討論：

-   [VSS 還原狀態](vss-restore-state.md)
-   [設定 VSS 還原方法](setting-vss-restore-methods.md)
-   [設定 VSS 還原目標](setting-vss-restore-targets.md)
-   [設定 VSS 還原選項](setting-vss-restore-options.md)

 (如需未使用這些機制之還原的相關資訊，請參閱不 [含寫入器參與的還原](restores-without-writer-participation.md)。 ) 

 

 



