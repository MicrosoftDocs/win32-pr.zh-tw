---
description: 如果 Windows Installer 套件安裝或通告元件，安裝程式會將這些元件的相關資訊儲存在本機系統登錄中。
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Windows Installer 所寫入的元件登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fd4a9bf3fa5e1eb557c2a179ec3e9a0853149ff197922a9fbf633a2869f41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746018"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Windows Installer 所寫入的元件登錄機碼

如果 Windows Installer 套件安裝或通告元件，安裝程式會將這些元件的相關資訊儲存在本機系統登錄中。 請注意，這些登錄機碼僅供 Windows Installer 在內部使用，且不應由您的應用程式來依賴。 這些機碼中儲存的資訊內容、位置和結構可能會變更。 應用程式應該依賴 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) 管理元件。

元件是由元件名稱所註冊。 儲存在下列位置的值名稱是元件名稱。 實際值的類型為 REG \_ 多重 \_ SZ，並且包含 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) 用來安裝或修復元件的資料。

## <a name="information-about-private-assemblies"></a>私用元件的相關資訊

Windows安裝程式會儲存在下列登錄機碼下安裝為受管理的每個使用者應用程式之 Windows Installer 套件所攜帶之私用元件的相關資訊：

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**安裝程式** \\**受控** \\**_使用者 SID_ *_\\_*** \\  \\ **_設定檔的_** 安裝程式元件路徑

Windows安裝程式會在下列登錄機碼下，儲存依使用者安裝的 Windows Installer 套件所攜帶的私用元件的相關資訊：

**HKCU** \\**軟體** \\**Microsoft** \\**安裝程式** \\**元件** \\**_設定檔案的路徑_**

Windows安裝程式會儲存 Windows Installer 套件隨附之私用元件的相關資訊，並在下列登錄機碼下依電腦安裝：

**HKLM** \\**軟體** \\**類別** \\**安裝程式** \\**元件** \\**_設定檔案的路徑_**

## <a name="information-about-global-or-shared-assemblies"></a>全域或共用元件的相關資訊

Windows安裝程式會儲存在下列登錄機碼下安裝為受管理的每個使用者應用程式之 Windows Installer 套件所攜帶的共用元件的相關資訊：

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**安裝程式** \\**受控** \\**_使用者 SID_ *_\\_* 全域安裝** \\ **程式元件** \\ 

Windows安裝程式會儲存在下列登錄機碼下，已針對每位使用者安裝的 Windows Installer 套件所攜帶的共用元件的相關資訊：

**HKCU** \\**軟體** \\**Microsoft** \\**安裝程式** \\**元件** \\**全域**

Windows安裝程式會儲存 Windows Installer 套件所攜帶的共用元件的相關資訊，並在下列登錄機碼底下安裝每一部電腦的相關資訊：

**HKLM** \\**軟體** \\**類別** \\**安裝程式** \\**元件** \\**全域**

 

 



