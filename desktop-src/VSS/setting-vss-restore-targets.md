---
description: '>ivsscomponent 介面可讓寫入器精確微調以元件為基礎來還原檔案的方式。'
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: 設定 VSS 還原目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9378fe8175970a8ccacb196414f3afafbcd583ad74f9aca438a3e9b6cf6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394188"
---
# <a name="setting-vss-restore-targets"></a>設定 VSS 還原目標

[**>Ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面可讓寫入器精確微調以元件為基礎來還原檔案的方式。

因為還原期間的系統設定可能不是在備份期間所預期的，所以會提供還原目的機制。

它可讓寫入器呼叫 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) 來變更如何還原那些 [*明確包含*](vssgloss-e.md) 在備份元件檔中的元件。 這也會變更 [*隱含包含*](vssgloss-i.md)的那些元件所使用的還原機制。

在系統重新開機期間發生的檔案還原 (在 [**vss \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉值下，如果無法取代) ，則在重新開機時還原 \_ \_ \_ \_ 和 vss \_ RME 還原， \_ \_ \_ \_ \_ \_ 因為 **MoveFileEx** 將檔案複製到最終位置時沒有執行中的 vss 服務。

同樣地，VSS \_ RME \_ 自訂還原可能會受到影響，因為每個自訂還原都是指定的寫入器專屬的，而且可以選擇要考慮或忽略還原目標。

要求者和寫入器可以使用 [**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) 檢查元件集的還原目標。

[**>Ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 支援下列還原目標，可在元件集的元件上設定：

-   VSS \_ RT \_ 原始。 將遵守 [**VSS \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉所指定的還原方法。
-   VSS \_ RT \_ 替代。 這些檔案會還原至從現有替代位置對應決定的位置。 如果存在與元件集子元件中路徑相符的替代位置對應，請盡可能還原至替代位置;否則，會傳回錯誤。

 

 



