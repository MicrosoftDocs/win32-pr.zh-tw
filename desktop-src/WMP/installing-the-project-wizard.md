---
title: 安裝 Project Wizard
description: 安裝 Project Wizard
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 類型2線上商店、外掛程式
- Windows Media Player 線上商店、外掛程式嚮導
- 線上商店、外掛程式嚮導
- 輸入2線上商店、外掛程式嚮導
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- Windows Media Player 線上商店，安裝外掛程式嚮導
- 線上商店，安裝外掛程式嚮導
- 輸入2個線上商店，安裝外掛程式 wizard
- Windows Media Player 線上商店，安裝專案嚮導
- 線上商店，安裝專案嚮導
- 輸入2個線上商店，安裝專案嚮導
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，輸入2個線上商店
- 外掛程式，安裝外掛程式 wizard
- 外掛程式、外掛程式嚮導
- 外掛程式，安裝專案嚮導
- 外掛程式，專案嚮導
- Windows Media Player 外掛程式，請輸入2個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式，安裝外掛程式嚮導
- Windows Media Player 外掛程式，外掛程式嚮導
- Windows Media Player 外掛程式，安裝專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 安裝外掛程式嚮導
- 外掛程式嚮導
- 安裝專案嚮導
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f00e0430791fb36285ba365eed752083889f2b55bd126c4a588d2a506f58acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123518"
---
# <a name="installing-the-project-wizard"></a>安裝 Project Wizard

若要設定開發環境以建立 type 2 online store 外掛程式，您必須安裝下列專案：

-   Microsoft Visual Studio .net 2003 或更新版本
-   Windows Media Player 9 系列或更新版本
-   Windowssdk，包含 Windows Media Player sdk
-   線上商店外掛程式嚮導

## <a name="installing-the-wizard"></a>安裝精靈

使用下列步驟，在 Visual Studio 中安裝線上商店外掛程式 wizard。

1.  找出安裝 Windows SDK 的資料夾。 展開資料夾以查看其子資料夾，並流覽至 [範例 \\ 多媒體 \\ WMP \\ 嚮導服務] \\ 。
2.  找出下列三個檔案：
    -   wmpservices .vsz
    -   wmpservices 的 vsdir
    -   wmpservices .ico
3.  使用文字編輯器（例如記事本）編輯 wmpservices .vsz 檔。

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
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    切換 `<path to wmpservices directory goes here>` 至 wizard 檔案所在的路徑。

    例如，假設您有 Visual Studio 2008，而您的 wizard 檔案位於此處： C： \\ Program files \\ Microsoft sdk \\ Windows v2.0 \\ \\ 範例 \\ 多媒體 \\ WMP \\ \\ 的服務。 然後您的 wmpservices .vsz 檔案看起來會像這樣：

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  找出安裝 Visual Studio 的資料夾。 展開資料夾以查看其子資料夾，並尋找名為 vcprojects 的資料夾。
5.  將步驟2中列出的三個檔案複製到 vcprojects 資料夾。 現在已安裝精靈。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Type 2 線上商店的外掛程式**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




