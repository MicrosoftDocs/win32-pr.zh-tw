---
title: 準備您的開發環境
description: 準備您的開發環境
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314932"
---
# <a name="prepare-your-development-environment"></a>準備您的開發環境

若要以 C 或 c + + 撰寫 Windows 程式，您必須安裝 Microsoft Windows 軟體開發套件 (SDK) 或 Microsoft Visual Studio。 Windows SDK 包含編譯和連結應用程式所需的標頭和程式庫。 Windows SDK 也包含用來建立 Windows 應用程式的命令列工具，包括 Visual C++ 編譯器和連結器。 雖然您可以使用命令列工具來編譯和建立 Windows 程式，但建議您使用 Microsoft Visual Studio。 您可以在 [這裡](https://visualstudio.microsoft.com/downloads/)下載免費的 Visual Studio Community 下載，或 Visual Studio 其他版本的免費試用版。

Windows SDK 的每個版本都是以最新版本的 Windows 為目標，以及數個舊版本。 版本資訊會列出受支援的特定平臺，但除非您針對非常舊的 Windows 版本維護應用程式，否則您應該安裝最新版本的 Windows SDK。 您可以在 [這裡](https://developer.microsoft.com/windows/downloads/windows-10-sdk)下載最新的 Windows SDK。

Windows SDK 支援開發32位和64位應用程式。 Windows Api 的設計目的是要讓相同的程式碼可以針對32位或64位進行編譯，而不需要變更。

> [!Note]  
> Windows SDK 不支援硬體驅動程式開發，且此系列不會討論驅動程式開發。 如需有關撰寫硬體驅動程式的詳細資訊，請參閱 [使用 Windows 驅動程式開始使用](/windows-hardware/drivers/gettingstarted/)。

## <a name="next"></a>下一個

[Windows 編碼慣例](windows-coding-conventions.md)

## <a name="related-topics"></a>相關主題

* [下載 Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [下載 Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)