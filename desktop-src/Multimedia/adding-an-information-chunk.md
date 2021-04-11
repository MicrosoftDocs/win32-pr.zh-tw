---
title: 新增資訊區塊
description: 新增資訊區塊
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183649"
---
# <a name="adding-an-information-chunk"></a>新增資訊區塊

如果您的應用程式除了音訊和影片之外，還需要包含其他資訊，您可以建立資訊區塊，並將其插入至 capture 檔。 資訊區塊可以包含數種類型的資訊，包括著作權聲明的詳細資料、影片來源的識別，或外部時間資訊。 下列範例會在資訊區塊中儲存一個 SMPTE (社會（運動圖片和電視工程師）) 時間碼的外部時間資訊，並使用 [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) 宏將區塊新增至 capture 檔案。


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




