---
description: 您無法刪除修補程式應用程式可能需要存取原始安裝來源的所有情況。
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: 防止 Patch 要求存取原始安裝來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5dcadae12b733d76dee8c3acd5ec6af6169c47cfd8c7eeb22ad9693a75859a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376787"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>防止 Patch 要求存取原始安裝來源

您無法刪除修補程式應用程式可能需要存取原始安裝來源的所有情況。

遵循下列各點以將修補程式需要存取原始來源的可能性降至最低：

-   使用僅限整個檔案的修補程式。 這樣就不需要針對所有先前發行的檔案版本建立二進位修補程式。 請注意，整個檔案修補程式的大小通常會大於二進位修補程式。 您可以輕鬆地將修補程式設為整個檔案修補程式，方法是撰寫 IncludeWholeFilesOnly 屬性，其值為1， (修補程式建立屬性中的一個)  (PCP) 檔。
-   確定您的任何自訂動作都不會存取原始來源位置。
-   確定 ResolveSource 動作是 conditionalized，讓它只在必要時才執行，或者完全不存在。
-   填入所有未建立版本檔案的 [MsiFileHash 資料表](msifilehash-table.md) 。 Msifiler.exe 的 Windows Installer SDK 工具可以輕易地為您完成此作業。
-   確定所有檔案都具有正確的版本和語言資訊。 Msifiler.exe 的 Windows Installer SDK 工具可以輕易地為您完成此作業。

## <a name="source-requirements-when-patching"></a>修補時的來源需求

在下列情況下，可能需要存取原始安裝來源才能套用修補程式：

-   修補程式適用于目前從來源執行的功能。 在此情況下，此功能會從來源執行狀態轉換為本機狀態。
-   修補程式適用于遺失或損毀檔案的元件。
-   修補程式會套用至元件中的檔案，其中也包含沒有 MsiFileHash 專案的未建立版本檔案。 需要填入的 [MsiFileHash 資料表](msifilehash-table.md) ，以防止來自來源位置的不必要 recopying 未建立版本檔案。
-   修補程式是以 amus 或 emus 的 REINSTALLMODE 來套用。 這個選項很危險，因為它會執行檔案複製作業，而不論檔案版本為何。 這可能會導致檔案 reving，而且幾乎一律需要來源。 建議的 REINSTALLMODE 值為 omus reinstall。
-   遺漏產品的快取套件。 修補程式需要有快取的封裝。 快取的封裝會儲存在% windir% \\ Installer 資料夾中。
-   封裝是為了呼叫 [ResolveSource 動作](resolvesource-action.md)而撰寫的。 此動作通常應該避免或 conditionalized 適當，因為它的執行一律會導致存取來源。
-   套件具有可嘗試以某種方式存取來源的自訂動作。 最常見的範例是「類型23並行安裝」自訂動作。
    > [!Note]  
    > 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。

     

-   Patch 封裝是由二進位修補程式所組成，這些修補程式並不會套用到電腦上目前版本的檔案。

請考慮下列範例，其中 Windows Installer 在套用修補程式時需要存取原始來源：

1.  安裝 RTM 版本的產品範例。
2.  將 patch Qfe1 套用至電腦。 此修補程式1.0 版 Example.dll 版本1.1。
3.  提供新的 patch、Qfe2，它會將 Example.dll 更新至1.2 版和 obsoletes Qfe1 .msp。 不過，修補程式只會建立為目標1.0 版的 Example.dll，因為它是使用產品的 RTM 版本所產生。 Example.dll 1.2 版包含 Example.dll 1.1 版中所包含的修正程式，但在 RTM 和 QFE2 映射之間產生 .msp 檔案。 因此，當 Qfe2 套用至電腦時，Windows Installer 必須存取原始來源。 Example.dll 的二進位修補程式無法套用至1.1 版;它只能套用至1.0 版。 這會導致安裝程式 recopying 1.0 版的 Example.dll 從原始來源位置開始，以便順利套用修補程式。

## <a name="source-requirements-when-removing-a-patch"></a>移除修補程式時的來源需求

如果 Windows Installer 尚未儲存修補程式的基準資訊，可能需要存取原始安裝來源才能移除修補程式。 從 Windows Installer 3.0 開始，安裝程式會選擇性地儲存更新檔案時的相關基準資訊。 如需基準快取的詳細資訊，請參閱 [減少修補程式大小](reducing-patch-size.md) 。

 

 



