---
title: 指令碼命令
description: 指令碼命令
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK，指令碼命令
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 腳本，命令
- 腳本，資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024298"
---
# <a name="script-commands"></a>指令碼命令

Windows Media 格式 SDK 所支援的指令碼命令為簡單名稱和值字串組。 例如，一般的指令碼命令為 "URL"，Windows Media Player 和其他播放應用程式用來開啟網頁。 "URL" 命令的腳本配對的另一半包含有效的統一資源定位器 (URL) ，例如 `https://www.adatum.com` 。 此 SDK 的物件不提供任何特定命令的支援;您的應用程式必須包含邏輯，才能處理您使用的任何命令。 您可以使用 Windows Media Player 所支援的命令來維持與大部分播放程式的相容性。

您可以使用下列兩種方式之一來傳遞指令碼命令：在腳本資料流程或檔案標頭中。

## <a name="script-streams"></a>腳本資料流程

您可以在 ASF 檔案的資料流程中傳遞指令碼命令。 腳本資料流程中的每個範例都包含名稱/值組的兩個字串。 使用腳本資料流程的優點是，命令會以正確的呈現時間傳遞。

## <a name="script-commands-in-the-file-header"></a>檔案標頭中的指令碼命令

指令碼命令可包含在檔案標頭中，以在播放時進行抓取。 播放應用程式會負責在適當的時間執行指令碼命令。 在檔案標頭中使用指令碼命令的優點是，所有的指令碼命令都可供使用，然後才開始接收範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**使用指令碼命令**](using-script-commands.md)
</dt> </dl>

 

 




