---
title: 使用外掛程式 Wizard 開始使用
description: 使用外掛程式 Wizard 開始使用
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player 外掛程式，安裝外掛程式嚮導
- 外掛程式，安裝外掛程式 wizard
- 建立外掛程式，安裝外掛程式 wizard
- Windows Media Player外掛程式嚮導，安裝
- 安裝外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576577"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>使用外掛程式 Wizard 開始使用

若要設定開發環境以建立 Windows Media Player 外掛程式，您必須安裝下列專案：

-   Microsoft Visual Studio .net 2003 或更新版本
-   Windows Media Player 9 系列或更新版本
-   Windowssdk，包含 Windows Media Player sdk
-   Windows Media Player外掛程式嚮導

## <a name="installing-the-wizard"></a>安裝精靈

請執行下列步驟來安裝 Windows Media Player 外掛程式 Wizard。

1.  找出安裝 Windows SDK 的資料夾。 展開資料夾以查看其子資料夾，然後流覽至 [範例 \\ 多媒體 \\ WMP \\ \\ wmpwiz]。
2.  找出下列三個檔案：
    -   wmpwiz .vsz
    -   wmpwiz 的 vsdir
    -   wmpwiz .ico
3.  使用文字編輯器（例如記事本）編輯 wmpwiz .vsz 檔。

    尋找下列程式碼行：

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    `<VsWizardEngine version goes here>`根據您已安裝的 Visual Studio 版本，變更為下列其中一個值。

    

    | 值              | Visual Studio 版本   |
    |--------------------|-------------------------|
    | VsWizardEngine 7。1 | Visual Studio .NET 2003 |
    | VsWizardEngine 8。0 | Visual Studio 2005      |
    | VsWizardEngine 9。0 | Visual Studio 2008      |

    

     

    尋找下列程式碼行：

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    切換 `<path to wmpwiz directory goes here>` 至 wizard 檔案所在的路徑。

    例如，假設您有 Visual Studio 2008，而您的 wizard 檔案位於此處： C： \\ Program files \\ Microsoft sdk \\ Windows v2.0 \\ \\ 範例 \\ 多媒體 \\ WMP \\ \\ wmpwiz。 然後您的 wmpwiz .vsz 檔案看起來會像這樣：

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  找出安裝 Visual Studio 的資料夾。 展開資料夾以查看其子資料夾，並尋找名為 vcprojects 的資料夾。
5.  將步驟2中列出的三個檔案複製到 vcprojects 資料夾。 現在已安裝精靈。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立外掛程式](building-a-plug-in.md)
</dt> <dt>

[使用外掛程式嚮導搭配 Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




