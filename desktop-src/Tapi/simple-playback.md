---
description: 下列主題描述如何執行簡單的播放。
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: 簡單播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975322"
---
# <a name="simple-playback"></a>簡單播放

下列主題描述如何執行簡單的播放。

**執行簡單的播放**

1.  在呼叫層級選取檔案播放終端機。
2.  在 TAPI 通話上建立播放終端機。
3.  設定屬性：儲存的檔案名和類型。
4.  在檔案播放終端機上呼叫 [**start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) 方法以開始播放資料流程。

下列範例程式碼示範簡單的播放。

首先，使用 [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) 介面建立錄製的終端機。 這會指示 TSP/MSP 在此呼叫上執行檔案播放。 TSP/MSP 會建立應用程式要使用的終端機，並在成功時傳回。


```C++

```



從終端介面取得 [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) 介面指標，並用它來設定要播放的檔案名。


```C++
pMediaPlayback->Release();
```



假設檔案包含一個音訊串流，而且此呼叫具有 capture 音訊串流，檔案中的音訊內容將會在該資料流程上播放。

 

 



