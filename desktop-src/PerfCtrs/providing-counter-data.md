---
description: 在 Windows Vista 中，效能計數器會將新的架構 (2.0 版) 提供計數器資料。
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: 提供計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0a17a6c75a86a7ee86f26350b9ea7680f0ba08338dbe7dc18cd56a8c425ba3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793621"
---
# <a name="providing-counter-data"></a>提供計數器資料

透過 Windows 效能計數器發佈資料的軟體元件，稱為效能資料提供者。

Windows 支援兩種類型的效能資料提供者。 舊版效能資料提供者 (**V1 提供者**) 會使用 .INI 檔和效能 DLL 來執行。 新式效能資料提供者 (**V2 提供者**) 使用。男人 (XML 資訊清單) 和效能計數器提供者 Api。

## <a name="manifests"></a>資訊清單

新式效能資料提供者使用。男人 (XML 資訊清單) 來定義計數器資料，並使用效能計數器提供者 Api 來管理提供者內容中的資料。

使用資訊清單和效能計數器提供者 Api 來執行的提供者通常稱為 **V2 提供者**。

Windows 支援 Windows Vista 或更新版本上的使用者模式 V2 提供者。 如需使用者模式的詳細資料，請參閱 [使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)。

Windows 支援 Windows 7 或更新版本上的核心模式 V2 提供者。 如需核心模式的詳細資料，請參閱 [核心模式效能監視](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)。

## <a name="performance-dll-deprecated"></a>效能 DLL (已淘汰) 

在舊版效能計數器架構中，提供者會將效能 DLL 實作為在取用者的進程中執行的，以便在取用者要求時收集和提供計數器資料。 提供者使用初始化 (.INI) 檔和登錄專案來定義計數器和設定效能 DLL。

使用 .INI 檔案和效能 DLL 來執行的提供者通常稱為 **V1 提供者**。

> [!CAUTION]
> 雖然您仍然可以使用效能 DLL 來提供計數器資料，但此架構已被取代，因為效能和可靠性有顯著的限制。 此外，V1 提供者通常較難實行，因為它們需要傳送必須在取用者進程中執行的個別 DLL。

如需詳細資訊，請參閱 [使用效能 DLL 提供計數器資料](providing-counter-data-using-a-performance-dll.md)。
