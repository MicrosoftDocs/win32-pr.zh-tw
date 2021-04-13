---
title: 使用外掛程式嚮導搭配 Visual Studio
description: 使用外掛程式嚮導搭配 Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player 外掛程式，Visual Studio
- 外掛程式，Visual Studio
- 建立外掛程式，Visual Studio
- Windows Media Player 外掛程式嚮導] 中 Visual Studio
- Visual Studio，Windows Media Player 外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301235"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>使用外掛程式嚮導搭配 Visual Studio

安裝必要的元件之後，您可以快速地建立將作為起點的外掛程式。 下列步驟將引導您。

1.  啟動 Microsoft Visual Studio。
2.  **在 [檔案**] 功能表中，指向 [**新增**]，然後按一下 [**專案**]。
3.  在 [ **專案類型**] 中，選取 [ **Visual C++ 專案**]。
4.  在 [ **範本**] 中，選取 **Windows Media Player 外掛程式]**。
5.  輸入專案的名稱。
6.  輸入專案的位置。 這是您的專案檔案將複製到其中的資料夾。
7.  按一下 **[確定** ] 啟動精靈。
8.  選取您要建立的外掛程式類型。
9.  完成嚮導中其餘的任何對話方塊。
10. 使用 Visual Studio 開發環境來建立您的專案。
    > [!Note]  
    > 在 Windows Vista 和更新版本中，除非您以完整系統管理員存取權杖執行 Visual Studio，否則專案將不會成功建立。 以滑鼠右鍵按一下 Visual Studio 名稱或圖示，然後按一下 [以 **系統管理員身分執行**]。

     

嘗試建立專案之前，請務必設定您的開發環境，以指向您安裝 Windows SDK 的名稱包括和 Lib 資料夾。 您的編譯器和連結器將需要存取這些資料夾中的某些檔案。

如果您執行 Windows SDK 隨附的 Visual Studio 註冊公用程式，您的開發環境可能已經設定為指向 Windows SDK Include 和 Lib 資料夾。 否則，您必須手動設定開發環境。

若要手動設定 Visual Studio，請使用下列步驟。

1.  在 **[工具]** 功能表上，按一下 **[選項]** 。
2.  按一下 [ **專案和方案**]，然後按一下 [ **VC + + 目錄**]。
3.  在 [ **顯示目錄**] 下，按一下 [ **包含** 檔案] 或 [文檔 **庫** 檔案]。
4.  新增所需檔案的目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立外掛程式](building-a-plug-in.md)
</dt> </dl>

 

 




