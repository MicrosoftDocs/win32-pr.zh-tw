---
title: 還原點
description: 系統會建立還原點，以允許使用者選擇先前的系統狀態。 每個還原點都包含將系統還原至所選狀態所需的必要資訊。 還原點會在對系統進行金鑰變更之前建立。
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316093"
---
# <a name="restore-points"></a>還原點

系統會建立還原點，讓使用者選取先前的系統狀態。 每個還原點都包含將系統還原至所選狀態所需的資訊。 還原點會在對系統進行金鑰變更之前建立。

系統還原會自動管理配置給還原點的磁碟空間。 它會清除最舊的還原點，以騰出空間給新的還原點。 系統還原會根據硬碟的大小和電腦執行的 Windows 版本配置空間，如下表所示。

|Windows 版本 |硬碟 &nbsp; 大小 |系統還原空間 |
| --- | --- | --- |
|Windows 7 和更新版本 | > 64 GB |最多五% 的總磁碟空間，最大值為 10 GB，以較少者為准 |
|  | &le; 64 GB |最多三% 的總磁碟空間 |
|Windows Vista |  |最多15% 的總磁碟空間，或最多30% 的可用磁碟空間，以較少者為准 |
|Windows XP | >4 GB |最多12% 的總磁碟空間<br /><br />若要變更 Windows XP 中的最大儲存空間限制，請使用主控台中的 [ **系統** ] 專案。 |
|  | \< 4 GB |最高 400 MB |

## <a name="event-triggered-restore-points"></a>事件觸發的還原點

系統還原會在發生下列任何事件之前自動建立還原點：

- **應用程式安裝** (只適用于使用系統還原相容安裝程式) 的應用程式。 如果應用程式安裝造成系統問題，使用者可以將系統還原到安裝之前的狀態。
- **Windows Update 或自動更新安裝**。 Windows Update (之前稱為「自動更新」) 會自動下載並安裝 Windows 更新。 此外，它還提供簡單的方式讓使用者手動下載及安裝更新。 系統還原會在安裝更新之前（不論是自動或手動）建立還原點。
- **系統還原** 作業。 系統還原會在啟動任何還原作業之前，自動建立還原點做為備份。 例如，假設使用者不小心將 Windows 還原為不正確的還原點。 若要復原該還原，使用者可以將視窗還原至第一個還原點之前的還原點。 當 Windows 還原為初始狀態之後，使用者就可以重複此程式，這次請選取正確的還原點。

## <a name="scheduled-restore-points"></a>排程的還原點

使用者可以設定系統還原，以定期間隔建立還原點。 使用者也可以隨時從系統還原的使用者介面中，手動建立並命名還原點。 這些還原點會儲存並壓縮，並且可在還原點清單中使用。

在 Windows 7 和更新版本中，只有在前七天沒有建立任何其他還原點時，系統還原才會建立排定的還原點。 在 Windows Vista 中，如果當天沒有建立其他還原點，系統還原會每24小時建立一個檢查點。 在 Windows XP 中，系統還原每24小時會建立一個檢查點，而不考慮其他作業。

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>已知問題：安裝 Windows 10 更新之後，您無法將系統還原到還原點

考慮下列案例：

1. 您可以在乾淨的電腦上安裝 Windows 10。
1. 您會開啟 [系統保護]，然後建立名為 "R1" 的系統還原點。
1. 您可以安裝一或多個 Windows 10 更新。
1. 在更新完成安裝之後，您會將系統還原至「R1」還原點。

在此案例中，系統不會還原至「R1」還原點。 相反地，電腦會發生停止錯誤 (0xc000021a) 。 您重新開機電腦，但系統無法返回 Windows 桌面。

### <a name="cause"></a>原因

這是 Windows 10 的已知問題。

在系統還原過程中，Windows 會暫時暫存正在使用中的檔案還原。 然後，它會將資訊儲存在登錄中。 當電腦重新開機時，它會完成暫存的操作。

在此情況下，Windows 會在電腦重新開機時還原類別目錄檔案，以及將驅動程式 ( sys) 檔案的階段。 但是，當電腦重新開機時，Windows 會先載入現有的驅動程式，然後再還原較新版的驅動程式。 因為驅動程式版本不符合已還原類別目錄檔案的版本，所以會停止重新開機進程。

### <a name="workaround"></a>因應措施

**從失敗的重新開機復原並繼續還原程式**

發生失敗後，請重新開機電腦，直到進入 Windows 修復環境 (WinRE) 。 若要這樣做，您可能必須使用硬體重新開機切換，而且可能需要重新開機多次。

在 Windows 修復環境中：

1. 選取 [**疑難排解**  >  **Advanced options**  >  **更多修復選項**  >  **啟動設定**]，然後選取 [**立即重新開機**]。
1. 在啟動設定清單中，選取 [ **停用驅動程式** 簽章強制]。
   > [!NOTE]  
   > 您可能必須使用 F7 鍵來選取此設定。
1. 讓啟動進程繼續進行。 當 Windows 重新開機時，系統還原程式應繼續執行並完成。

這些步驟會將電腦還原到其「R1」狀態。

**從失敗的重新開機復原**

若要從失敗的重新開機復原並復原還原程式，請遵循下列步驟：

1. 如先前程式中所述，重新開機電腦，然後輸入 WinRE。  
1. 在 Windows 修復環境中，選取 [**疑難排解**  >  **Advanced options**  >  **系統還原**]，然後選取 [**復原系統還原**]。

這些步驟會在您開始還原程式之前，將電腦恢復為其所在的狀態。

**使用 WinRE 將 Windows 還原至還原點**

若要在受影響的電腦上啟動系統還原 wizard，請使用 WinRE，而不是 [ **設定** ] 對話方塊。 若要這樣做，請遵循下列步驟：

1. 選取 [**啟動**  >  **設定**  >  **更新 & 安全性** 復原]  >  ****。
1. 在 [ **Advanced options**] 底下，選取 [ **立即重新開機**]。
1. WinRE 開始之後，請選取 [**疑難排解**  >  **Advanced options**  >  **系統還原**]。
1. 輸入您的修復金鑰（顯示在畫面上），然後依照系統還原 wizard 中的指示進行。

### <a name="references"></a>參考資料

如需有關如何使用 WinRE 的詳細資訊，請參閱下列文章：

- [Windows 修復環境 (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [在 Windows 10 中以安全模式啟動電腦](https://support.microsoft.com/help/12376) 