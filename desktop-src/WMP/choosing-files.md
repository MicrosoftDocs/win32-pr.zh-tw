---
title: 選擇檔案
description: 選擇檔案
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- 建立外觀，選擇檔案
- Windows Media Player 的外觀，選擇檔案
- 外觀，選擇檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183951"
---
# <a name="choosing-files"></a>選擇檔案

如果您想要選擇檔案，您可以使用類似播放清單範例的程式碼，但請將下列內容取代為 PLAYELEMENT 區段：


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



這一行會使用 **主題** 的 **openDialog** 方法來定義播放程式的 **URL** 。 您可以使用這個來選擇不在播放清單中的檔案。

您可以在 SDK 的範例區段中看到類似的工作 **openDialog** 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




