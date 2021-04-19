---
description: 瞭解如何使用標準使用者分析器 (SUA) tool 和 SUA Wizard 來測試您的應用程式，並偵測潛在的相容性問題。
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: 標準使用者分析器 (SUA) 工具和標準使用者分析器精靈 (SUA 精靈)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314581"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>標準使用者分析器 (SUA) 工具和標準使用者分析器精靈 (SUA 精靈)

## <a name="affected-platforms"></a>受影響的平臺

**用戶端：** Windows XP、Windows Vista、Windows 7  
**伺服器：** Windows Server 2003、Windows Server 2008、Windows Server 2008 R2  

## <a name="description"></a>描述

應用程式相容性工具組包含標準使用者分析器 (SUA) 工具和標準使用者分析器 Wizard (SUA Wizard) 。 這些工具可讓您測試應用程式，並監視 API 呼叫，以便偵測由於 Windows 7 作業系統中的使用者帳戶控制 (UAC) 功能所造成的潛在相容性問題。

UAC （先前稱為受限的使用者帳戶 (LUA) ）要求 (包括系統管理員群組成員的所有使用者) 以標準使用者身分執行，直到蓄意提高應用程式的許可權。 不過，需要存取權的應用程式以及標準使用者無法使用之位置的許可權，無法正常執行標準使用者角色。

## <a name="usage"></a>使用方式

下列各節提供有關如何使用 SUA 和 SUA Wizard 工具的詳細資訊。

**SUA 工具**

SUA 工具可讓您分析應用程式、查看有關 UAC 相關問題的詳細報告，然後套用建議和選取的應用程式緩和措施，如下列流程圖所示。

![顯示 S U 工具的流程的圖表。](images/act-suaflowchart-appcookbook.gif)

*SUA 工具和虛擬化*

只有 SUA 工具可讓您開啟和關閉虛擬化功能。 藉由關閉虛擬化功能，經過測試的應用程式在 Windows XP 作業系統上運作時的行為就會更類似。

*SUA 工具和更高的許可權*

只有 SUA 工具可讓您開啟和關閉 **啟動較高** 的功能。 啟動提高許可權功能可讓選取的應用程式以系統管理員或標準使用者身分執行。 根據您的選擇，您會找到與 UAC 相關的不同類型問題。 如果您清除 [提高 **許可權啟動** ] 核取方塊，您的應用程式將會以完整系統管理員許可權執行，這可讓 SUA 預測標準使用者可能發生的問題。 如果您選取 [提高許可權啟動] 核取方塊，您將會看到應用程式實際執行和產生錯誤所導致的錯誤。

**SUA Wizard**

SUA Wizard 可讓您遵循引導式逐步程式，讓您分析應用程式，然後套用建議和選取的應用程式緩和措施，如下列流程圖所示。 與 SUA 工具不同的是，嚮導不會啟用有關 UAC 相關問題的評論。

![顯示 S U Wizard 流程的圖表。](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>其他資源的連結

-   [應用程式相容性工具組下載](/windows-hardware/get-started/adk-install)
-   [瞭解標準使用者分析器工具](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [標準使用者分析器技術參考](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [使用開發工具測試和緩和問題](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [應用程式相容性與使用者帳戶控制](/previous-versions/windows/)

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
