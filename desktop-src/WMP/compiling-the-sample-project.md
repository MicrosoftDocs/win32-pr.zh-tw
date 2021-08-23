---
title: 編譯範例 Project
description: 編譯範例 Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player 線上商店，編譯範例專案
- 線上商店，編譯範例專案
- 輸入2個線上商店，編譯範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- 外掛程式，專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 編譯範例專案
- 範例，請輸入2個線上商店
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763938"
---
# <a name="compiling-the-sample-project"></a>編譯範例 Project

Wizard 會產生編譯範例專案所需的所有檔案，因此您不需要變更預設的專案設定。 在 Visual Studio 中，按一下 [**組建**] 功能表上的 [**建立方案**]，以建立並註冊 COM 元件。 根據預設，偵錯工具設定為使用中狀態。

> [!Note]  
> 在 Windows Vista 和更新版本中，除非您以完整系統管理員存取權杖執行 Visual Studio，否則專案將不會成功建立。 以滑鼠右鍵按一下 Visual Studio 名稱或圖示，然後按一下 [以 **系統管理員身分執行**]。

 

嘗試建立專案之前，請務必設定您的開發環境，以指向您安裝 Windows SDK 的名稱包括和 Lib 資料夾。 您的編譯器和連結器將需要存取這些資料夾中的某些檔案。

如果您執行 Windows Vista SDK 隨附的 Visual Studio 註冊公用程式，您的開發環境可能已經設定為指向 Windows SDK Include 和 Lib 資料夾。 否則，您必須手動設定開發環境。

若要手動設定 Visual Studio，請使用下列步驟。

1.  在 **[工具]** 功能表上，按一下 **[選項]** 。
2.  按一下 [**專案和方案**]，然後按一下 [ **VC++ 目錄**]。
3.  在 [ **顯示目錄**] 下，按一下 [ **包含** 檔案] 或 [文檔 **庫** 檔案]。
4.  新增所需檔案的目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Type 2 線上商店的外掛程式](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




