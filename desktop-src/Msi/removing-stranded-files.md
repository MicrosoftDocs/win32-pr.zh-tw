---
description: Windows Installer 卸載無法移除應用程式的所有檔案的可能原因清單。
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: 移除擱置的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1209d1e79c901b7ba29c374bb9fcc51c74d0156f87b5251760f789e843f2387d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990688"
---
# <a name="removing-stranded-files"></a>移除擱置的檔案

如果在執行卸載後，應該從使用者的電腦移除的檔案仍保持安裝，則安裝程式可能會因為下列一或多個原因而無法移除包含檔案的元件：

-   在 [元件資料表](component-table.md)的 [屬性] 資料行中，已設定元件的 msidbComponentAttributesPermanent 位。
-   未在元件資料表的 [元件] 資料行中輸入元件的值。
-   另一個仍安裝的應用程式或功能會使用此元件。
-   [條件](condition-table.md)資料表中指定的條件會在安裝期間啟用功能，並在卸載期間停用此功能。
-   元件的金鑰檔在 **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **shareddll** 底下有先前的參考計數。
-   元件會安裝在系統資料夾中，而且元件中的任何檔案在 **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **shareddll** 下都有先前的參考計數。
-   Windows Installer 不會移除[Windows 資源保護](../wfp/windows-resource-protection-portal.md) (WRP) 所保護的任何檔案或登錄機碼。 如需詳細資訊，請參閱[使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。 在 Windows Server 2003、Windows XP 和 Windows 2000 上，安裝程式並不會移除 Windows 檔案保護 (WFP) 所保護的任何檔案。 如果元件的金鑰路徑檔案或登錄機碼受到 WFP 或 WRP 的保護，安裝程式就不會移除該元件。
    > [!Note]  
    > 因為 Windows Installer 不會安裝、更新或移除任何受 WRP 保護的資源，所以您不應該在安裝套件中包含受保護的資源。 相反地，請只使用[Windows 資源保護](../wfp/windows-resource-protection-portal.md)一節中所述的[支援資源取代機制](../wfp/supported-file-replacement-mechanisms.md)。

     

 

 
