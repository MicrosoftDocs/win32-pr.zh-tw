---
description: ForceReboot 動作會在安裝期間提示使用者重新開機系統。
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: ForceReboot 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41af6b656222a31ab75c9df3f2fa9f94af415f94d6d0b50010c0b25c5742502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636069"
---
# <a name="forcereboot-action"></a>ForceReboot 動作

ForceReboot 動作會在安裝期間提示使用者重新開機系統。 ForceReboot 動作與 [ScheduleReboot 動作](schedulereboot-action.md) 不同，因為 ScheduleReboot 動作是用來排定在安裝結束時重新開機的提示。

如果安裝具有使用者介面，安裝程式會在每個 ForceReboot 動作顯示對話方塊，提示使用者重新開機系統。 使用者必須在繼續安裝之前回應此提示。 如果安裝沒有使用者介面，系統會自動重新開機 ForceReboot 動作。

如果安裝程式判斷是否需要重新開機，它會在安裝結束時自動提示使用者重新開機，不論順序中是否有任何 ForceReboot 或 ScheduleReboot 動作。 例如，安裝程式會在需要取代安裝期間所使用的任何檔案時，自動提示重新開機。

藉由設定 [ [**重新開機**](reboot.md) ] 屬性來抑制特定的重新開機提示。

如果 Windows Installer 在[多套件安裝](multiple-package-installations.md)期間遇到 ForceReboot 或[ScheduleReboot](schedulereboot-action.md)動作，安裝程式將會停止並復原安裝。 您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。

## <a name="sequence-restrictions"></a>順序限制

下列動作通常會一起作為動作順序中的群組。 建議您將 ForceReboot 動作排定在此群組之後。 如果 ForceReboot 動作是在 [RegisterProduct 動作](registerproduct-action.md)之前排程，則安裝程式會在重新開機後再次要求安裝套件的來源。 因此，ForceReboot 的慣用順序會緊接在此動作序列之後。

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

ForceReboot 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)的動作順序中的[InstallInitialize](installinitialize-action.md)和[InstallFinalize](installfinalize-action.md)之間。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

ForceReboot 動作必須一律搭配條件陳述式使用，讓安裝程式只在必要時才觸發重新開機。 例如，只有在已取代特定檔案或安裝特定元件時，才可能需要重新開機。 每個產品安裝都是唯一的，而且可能需要進行自訂動作，以判斷是否需要重新開機。 ForceReboot 動作的條件通常會使用 [**AFTERREBOOT**](afterreboot.md) 屬性。

ForceReboot 會在提示重新開機或重新開機之前，執行任何先前動作所產生的系統作業。 例如， [InstallFiles](installfiles-action.md) 和 [WriteRegistryValues](writeregistryvalues-action.md) 所產生的系統作業會在重新開機之前執行。

ForceReboot 動作會寫入登錄機碼，以便在重新開機後啟動安裝程式。 此金鑰的位置是 **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系統重新開機](system-reboots.md)
</dt> </dl>

 

 



