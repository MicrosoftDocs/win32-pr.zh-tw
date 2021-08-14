---
title: 使用指令碼命令
description: 使用指令碼命令
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows媒體格式 SDK，指令碼命令
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- 腳本，命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195784"
---
# <a name="using-script-commands"></a>使用指令碼命令

Windows 媒體格式 SDK 支援使用指令碼命令來通訊 ASF 檔案中的應用程式動作。 每個指令碼命令都是由兩個字串所組成，第一個字串是命令的類型，第二個是命令資料。 例如，您可以使用「URL」腳本類型，並傳遞有效的網際網路 URL 做為命令資料。 當支援型別為 "URL" 之指令碼命令的讀取應用程式收到此命令時，會在瀏覽器視窗中開啟指定的位址。

Windows 媒體格式 SDK 提供兩個選項，可讓您在 ASF 檔案中傳遞腳本。 您可以建立腳本資料流程，也可以在檔案的標頭中包含指令碼命令。 腳本資料流程很有用，因為指令碼命令會以展示時間順序傳遞。 如果您在檔案標頭中使用指令碼命令，則您的應用程式必須在開始播放之前，先取出所有的指令碼命令。 您必須追蹤指令碼命令的呈現時間，並在適當的時間進行回應。

下列各節說明如何在 ASF 檔案中包含指令碼命令。



| 區段                                                                                                                | 描述                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [使用腳本資料流程](to-use-a-script-stream.md)                                                                   | 描述如何在腳本資料流程中包含指令碼命令。 |
| [將腳本資料新增至標頭](to-add-script-data-to-the-header.md)                                               | 描述如何在檔案標頭中包含指令碼命令。 |
| [使用 Windows Media Player 所支援的指令碼命令](using-script-commands-supported-by-windows-media-player.md) | 描述 Windows Media Player 所使用的指令碼命令。  |



 

> [!Note]  
> 在舊版的 Windows 媒體格式 SDK 中，腳本串流是用來開啟對應至 ASF 檔案內容的網頁位址。 您現在可以使用 Web 資料流程來處理已同步處理的網頁。 如需詳細資訊， 請參閱 [Web 串流](web-streams.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**指令碼命令**](script-commands.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 




