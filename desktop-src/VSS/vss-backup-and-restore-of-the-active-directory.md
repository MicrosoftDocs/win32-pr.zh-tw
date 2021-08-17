---
description: Active Directory 寫入器在備份作業期間不需要執行任何特殊動作。
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Active Directory 的 VSS 備份和還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751481"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Active Directory 的 VSS 備份和還原

Active Directory 寫入器在備份作業期間不需要執行任何特殊動作。 寫入器會提供元件和檔案集資訊給要求者，而要求者會使用該資訊來決定要複製到備份媒體的檔案。 不需要使用任何特殊的 Api 來備份 Active Directory。

執行還原的方式取決於 Active Directory 是否要在發生嚴重損壞修復作業時還原，或還原到執行 Active Directory 的系統。 此外，Active Directory 狀態的備份副本存留期可能會因為 Active Directory 的標記而發生問題。

## <a name="active-directory-restoration-following-disaster-recovery"></a>在嚴重損壞修復之後 Active Directory 還原

在需要嚴重損壞修復的損毀之後，Active Directory 可以還原為作業系統狀態還原的一部分。

這項還原作業基本上是 writerless 還原。

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory 正在執行的系統上還原

如果 Active Directory 目前正在伺服器上執行，則必須以目錄服務還原模式重新開機系統。

作業系統會在沒有 Active Directory 的情況下執行，而所有使用者驗證都會透過登錄中的安全性帳戶管理員 (SAM) 進行。 只有系統管理員才有復原 Active Directory 的許可權。

進入目錄服務還原模式之後，就可以正常進行 VSS 還原。 沒有理由使用非 VSS Win32 Active Directory Api 來還原 Active Directory 狀態。

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory 還原和 Active Directory 的標記

任何復原方案都應該確保備份的存留期不應超過 Active Directory 的標記存留期 (預設值為60天) 。

還原超過標記的備份將會導致網域控制站有不會複寫到其他伺服器的物件。

未複寫的物件將不會在該 (還原) 網域控制站上自動刪除，因為已刪除其他複本上的那些物件的標記。

系統管理員必須手動刪除未複寫的已還原網域控制站上的每個物件。 不支援 Active Directory 的增量備份;需要完整備份。

 

 



