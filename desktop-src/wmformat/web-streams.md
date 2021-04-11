---
title: Web 串流
description: Web 串流
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK，Web 資料流程
- Advanced Systems Format (ASF) 、Web 串流
- ASF (Advanced Systems Format) ，Web 串流
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- Web 串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021377"
---
# <a name="web-streams"></a>Web 串流

Web 資料流程就像是檔案資料流程，它包含資料檔案。 在 Web 資料流程中，這些檔案通常是 HTML 網頁以及 GIF 或 JPEG 格式的相關圖形。

Web 串流特別適用于以簡報形式使用的 ASF 檔案。 在支援 Web 串流之前，簡報在檔案內的腳本資料流程中會有 Url，讓網頁可以在預定的時間載入。 困難之處在于網路擁塞可能會造成延遲，並建立不佳的觀賞體驗。

使用 Web 串流時，Web pages 的組成部分可以包含在 ASF 檔案中作為串流。 當收到檔案時，可以快取這些檔案，如此一來，當命令顯示 (或轉譯) URL 時，瀏覽器就可以立即存取這些檔案。 這可讓您順暢且一致地播放。 轉譯命令會在 Web 資料流程本身中傳遞，而不是在個別資料流程中以指令碼命令的形式傳遞。

建議使用 Windows Media Format 9 系列 SDK 建立的 Web 串流，或稍後為版本號碼1提供。 這個值是在 **wVersion** 成員的 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)結構中指定的。 SDK 本身不會執行任何動作來強制執行此版本。

> [!Note]  
> 連接到具有 Web 串流的即時廣播串流時，使用者可能會在指定的檔案實際位於本機快取之前，收到轉譯命令。 除非您的應用程式會處理這種狀況，否則瀏覽器會顯示「找不到頁面」錯誤。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**任意資料流程**](arbitrary-streams.md)
</dt> <dt>

[**設定 Web 資料流程**](configuring-web-streams.md)
</dt> </dl>

 

 




