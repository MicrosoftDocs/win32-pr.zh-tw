---
title: 準備您的開發環境
description: 準備您的開發環境
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896968"
---
# <a name="prepare-your-development-environment"></a>準備您的開發環境

若要使用 c 或 c + + 撰寫 Windows 程式，您必須安裝 Microsoft Windows 軟體開發套件 (SDK) 或 Microsoft Visual Studio。 Windows SDK 包含編譯和連結應用程式所需的標頭和程式庫。 Windows SDK 也包含用來建立 Windows 應用程式的命令列工具，包括 Visual C++ 編譯器和連結器。 雖然您可以使用命令列工具編譯和建立 Windows 程式，但我們建議使用 Microsoft Visual Studio。 您可以在[這裡](https://visualstudio.microsoft.com/downloads/)下載免費的 Visual Studio Community 下載，或 Visual Studio 其他版本的免費試用版。

Windows SDK 的每個版本都以最新版本的 Windows 以及數個舊版為目標。 版本資訊會列出受支援的特定平臺，但除非您要針對非常舊版的 Windows 維護應用程式，否則您應該安裝最新版本的 Windows SDK。 您可以在[這裡](https://developer.microsoft.com/windows/downloads/windows-10-sdk)下載最新的 Windows SDK。

Windows SDK 支援開發32位和64位應用程式。 Windows api 的設計目的是要讓相同的程式碼可以針對32位或64位進行編譯，而不需要變更。

> [!Note]  
> Windows SDK 不支援硬體驅動程式開發，且此系列不會討論驅動程式開發。 如需有關撰寫硬體驅動程式的詳細資訊，請參閱[Windows 驅動程式的開始使用](/windows-hardware/drivers/gettingstarted/)。

## <a name="next"></a>下一個

[Windows編碼慣例](windows-coding-conventions.md)

## <a name="related-topics"></a>相關主題

* [下載 Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [下載 Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)