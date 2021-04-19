---
description: 從 Windows Installer&\# 160; 版本&\# 160; 3.0 開始，可以建立並安裝可單獨卸載的修補程式，而不需要卸載並重新安裝整個應用程式和其他修補程式。
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: 移除修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977977"
---
# <a name="removing-patches"></a>移除修補程式

從 Windows Installer 版本3.0 開始，您可以建立並安裝可單獨卸載的修補程式，而不需要卸載並重新安裝整個應用程式和其他修補程式。 Windows Installer 3.0 也可讓您使用包含修補程式順序資訊的[MsiPatchSequence 資料表](msipatchsequence-table.md)來撰寫[修補封裝](patch-packages.md)。 在 Windows Installer 3.0 之前的 Windows Installer 版本中，從應用程式移除特定修補程式的唯一方法，就是卸載整個已修補的應用程式，然後重新安裝，而不需要重新套用任何即將移除的修補程式。

是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。 如果未可卸載修補程式，則移除修補程式的唯一方法是卸載整個應用程式，並重新安裝，而不套用即將移除的修補程式。

您可以使用命令列選項、指令碼介面，或從另一個應用程式呼叫 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) ，來卸載一或多個修補程式。 如需如何卸載修補程式的詳細資訊，請參閱 [卸載修補程式](uninstalling-patches.md) 。

[**MSIPATCHREMOVE**](msipatchremove.md)屬性的值會列出要卸載的修補程式。 針對清單中的每個修補程式，安裝程式會驗證是否已可卸載修補程式。 如果使用者沒有移除修補程式的許可權、修補程式對產品而言是未知的、修補原則會防止移除，或修補程式標示為未可卸載，安裝程式會傳回錯誤，指出安裝失敗的交易。 如需判斷是否有修補程式未可卸載的詳細資訊，請參閱 [可卸載修補程式](uninstallable-patches.md) 。

一旦將修補程式驗證為卸載式，安裝程式就會從 patch 應用程式順序中移除修補程式。 如需 Windows Installer 3.0 如何判斷套用修補程式時所要使用之順序的詳細資訊，請參閱 [排序修補程式](sequencing-patches.md)。 請注意，從序列中移除修補程式可能會導致標示為已淘汰或被取代的修補程式變成作用中。

選取要移除的所有修補程式都會列在 [**MsiPatchRemovalList**](msipatchremovallist.md) 屬性中。 這個屬性是由安裝程式所設定的私用屬性，可用於條件運算式或 [自訂動作](custom-actions.md)查詢。 屬性包含要移除之修補程式的修補程式程式碼 Guid 清單。 自訂動作可以藉由呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)或 [Patch 物件](patch-object.md)的 [**PatchProperty**](patch-patchproperty.md)屬性，來決定是否要套用、淘汰或取代修補程式的安裝狀態。

移除修補程式之後，應用程式的狀態就會和從未安裝過修補程式一樣。 如果可能的話，安裝程式會將處理常式限制為遭移除的修補程式所影響的功能子集。 安裝程式會自動將 [ [**重新安裝**](reinstall.md) ] 屬性設定為受影響功能的清單。 系統會移除修補程式所新增的檔案，並覆寫修補程式所修改的檔案。 檔案和登錄專案會還原至產品所預期的版本減去修補程式。 修補程式所加入的功能和元件會從應用程式取消註冊。 請注意，如果另一個仍適用的修補程式使用內容，修補程式新增的其他內容可以保留在使用者的電腦上。

如果有修補程式更新共用元件的檔案，此變更會影響共用元件的所有應用程式。 移除修補程式時，此變更會影響共用元件的所有應用程式。 這表示，將修補程式移除一個應用程式，可以將共用元件的檔案還原至比其他應用程式所需的版本更低的版本。 這可以修正第一個應用程式，但會導致第二個應用程式停止運作。 在此情況下，您可以使用 [重新安裝功能或應用程式](reinstalling-a-feature-or-application.md)中所述的方法，重新安裝第二個應用程式，以修復第二個應用程式。 這會還原檔案的已修補版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[修補程式順序](sequencing-patches.md)
</dt> <dt>

[修補卸載自訂動作](patch-uninstall-custom-actions.md)
</dt> <dt>

[可卸載修補程式](uninstallable-patches.md)
</dt> <dt>

[卸載修補程式](uninstalling-patches.md)
</dt> </dl>

 

 



