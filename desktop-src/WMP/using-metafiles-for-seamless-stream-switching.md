---
title: 使用中繼檔進行順暢的串流切換
description: 使用中繼檔進行順暢的串流切換
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Windows媒體中繼檔播放清單，實況活動資料流切換
- 播放清單、實況活動資料流切換
- 中繼檔播放清單，即時事件資料流程切換
- Windows媒體中繼檔播放清單，事件資料流程切換
- 播放清單、事件資料流程切換
- 中繼檔播放清單，事件資料流程切換
- Windows媒體中繼檔播放清單，廣告插入
- 播放清單、廣告插入
- 中繼檔播放清單，廣告插入
- Windows Media Player，即時事件串流切換
- Windows Media Player，事件資料流程切換
- Windows Media Player，ad 插入
- 即時事件資料流程切換
- 事件資料流程切換
- 廣告插入
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4efc4a23f0464446675d9de20d57750bd230d2eef26d31714e2129e380ae9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001568"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>使用中繼檔進行順暢的串流切換

您可以使用中繼檔播放清單來加速順暢的串流切換。 通常，當內容結束時，下一個剪輯或串流在開啟之前會先進行緩衝處理，然後才會開啟 (如果是從串流媒體伺服器收到的內容) 。 Microsoft Windows Media Services 可讓您將此緩衝處理時間降至最低，或至少減少最小化，並立即開始播放另一段串流內容。 Windows Media Player 的正常操作模式是開啟播放清單在目前轉譯的資料流程結束前20秒所參考的下一個媒體資料流程。 這通常會在媒體串流之間提供順暢的轉換，這取決於其他因素，例如 Web 存取時間。

使用播放清單中的 **事件** 專案搭配編碼器中的 OPENEVENT 命令，以促進資料流程或檔案之間的流暢切換。 在事件命令之前的20秒或更多時間內傳送 OPENEVENT 命令可將串流切換的延遲降至最低。 然後 Windows Media Player 可以將即將推出的串流內容的一部分預先載入緩衝區。

使用 Windows 媒體編碼器，在資料流程中使用下列格式傳送指令碼命令：


```XML
OPENEVENT eventname 

```



事件名稱必須是播放清單中 **事件** 元素中定義的名稱。 當 Windows Media Player 從編碼器接收 OPENEVENT 指令碼命令時，會查看播放清單中的 **事件** 專案，並開始緩衝處理 **事件** 元素中定義的剪輯或資料流程。 Windows Media Player 接著保存此資訊，直到相同名稱的實際事件為止。 收到指名的事件時，Windows Media Player 會切換至先前已緩衝處理的內容。

> [!Note]  
> 您無法在媒體檔案或播放清單中的 **事件** 元素中使用 Unicode 字元作為 OPENEVENT 指令碼命令。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**ScriptCommand 事件**](player-player-scriptcommand.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




