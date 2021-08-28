---
title: 使用 Windows Media Player 所支援的指令碼命令
description: 使用 Windows Media Player 所支援的指令碼命令
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows媒體格式 SDK，指令碼命令
- Windows媒體格式 SDK，Windows Media Player
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- Advanced Systems Format (ASF) ，Windows Media Player
- ASF (Advanced Systems Format) ，Windows Media Player
- 腳本，命令
- 腳本，Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110068"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>使用 Windows Media Player 所支援的指令碼命令

Windows 媒體格式 SDK 不提供剖析和回應指令碼命令的原生支援。 您必須在應用程式中包含與指令碼命令相關的任何邏輯。 您也必須在應用程式中定義您使用的腳本類型。

您可以包含程式碼來處理 Windows Media Player 所支援的相同指令碼命令。 維持與 Windows Media Player 的相容性，可讓您的檔案比內嵌自訂指令碼命令更通用。

下表列出 Windows Media Player 所支援的腳本類型。



| 指令碼類型 | 描述                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | 播放程式會將指定的 URL 傳送給瀏覽器，以顯示給使用者。 如果使用內嵌播放機控制項，您可以使用 &&*framename* 語法，將特定的框架參考加入至 URL。                                                                             |
| 檔案名    | 另一個要播放之媒體檔案的 URL。                                                                                                                                                                                                                                                |
| CAPTION     | 顯示在 Windows Media Player 的標題區域中的文字字串。 此類型支援標準 HTML 格式，因此可以依您的需要將文字格式化。 使用的範例有隱藏式輔助字幕。                                                                             |
| 事件       | 要發生之事件的名稱。 事件種類支援自訂您自己的用途。 指定事件的程式碼必須定義于資料流程的 Windows 媒體中繼檔中，才能讓播放程式執行指定的事件。 使用的範例是 ad 插入。 |
| OPENEVENT   | 此腳本會在實際事件之前。 OPENEVENT 可讓播放程式預先緩衝處理內容，如此一來，當事件發生時，資料流程之間的切換就看起來很順暢。                                                                                                       |
| TEXT        | 顯示在 Windows Media Player 的標題區域中的文字字串。 可以是純文字、薩米文或 HTML 格式的文字。                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用指令碼命令**](using-script-commands.md)
</dt> </dl>

 

 




