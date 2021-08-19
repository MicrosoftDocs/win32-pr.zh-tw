---
title: 使用線上商店外掛程式嚮導搭配 Visual Studio
description: 使用線上商店外掛程式嚮導搭配 Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 輸入1個線上商店、外掛程式
- Windows Media Player 線上商店、外掛程式嚮導
- 線上商店、外掛程式嚮導
- 輸入1線上商店、外掛程式嚮導
- Windows Media Player 線上商店，Visual Studio
- 線上商店、Visual Studio
- 輸入1個線上商店，Visual Studio
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，請輸入1個線上商店
- 外掛程式，Visual Studio
- 外掛程式、外掛程式嚮導
- Windows Media Player 外掛程式，請輸入1個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式，Visual Studio
- Windows Media Player 外掛程式，外掛程式嚮導
- Visual Studio，Windows Media Player 線上商店嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830679"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>使用線上商店外掛程式嚮導搭配 Visual Studio

安裝必要的元件之後，您可以快速地建立將作為起點的外掛程式。 下列步驟將引導您：

1.  啟動 Microsoft Visual Studio。
2.  **在 [檔案**] 功能表中，指向 [**新增**]，然後按一下 [ **Project**]。
3.  在 **Project 類型**] 中，按一下 [ **Visual C++ 專案**]。
4.  在 [**範本**] 中，按一下 [**線上商店] Windows Media Player**。
5.  輸入專案的名稱。
6.  輸入專案的位置。 這是您的專案檔案將複製到其中的資料夾。
7.  按一下 **[確定** ] 啟動精靈。
8.  選取 [ **類型 1 (深層整合])**，然後按 **[下一步]**。
9.  輸入易記名稱和內容散發者。 按一下 [完成]  。
10. 使用 Visual Studio 開發環境來建立您的專案。
    > [!Note]  
    > 在 Windows Vista 和更新版本中，除非您以完整系統管理員存取權杖執行 Visual Studio，否則專案將不會成功建立。 以滑鼠右鍵按一下 Visual Studio 名稱或圖示，然後按一下 [以 **系統管理員身分執行**]。

     

嘗試建立專案之前，請務必設定您的開發環境，以指向您安裝 Windows SDK 的名稱包括和 Lib 資料夾。 您的編譯器和連結器將需要存取這些資料夾中的某些檔案。

如果您執行 Windows SDK 隨附的 Visual Studio 註冊公用程式，您的開發環境可能已經設定為指向 Windows SDK Include 和 Lib 資料夾。 否則，您必須手動設定開發環境。

若要手動設定 Visual Studio，請使用下列步驟。

1.  按一下 [ **工具** ] 功能表上的 [選項]。
2.  按一下 [**專案和方案**]，然後按一下 [ **VC++ 目錄**]。
3.  在 [ **顯示目錄**] 下，按一下 [ **包含** 檔案] 或 [文檔 **庫** 檔案]。
4.  新增所需檔案的目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類型1線上商店的外掛程式](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




