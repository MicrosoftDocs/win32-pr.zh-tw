---
title: 簡易音訊播放
description: 簡易音訊播放
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- 多媒體音訊、波形
- 音訊、波形
- 波形音訊，簡單播放
- MessageBeep 函式
- sndPlaySound 函式
- PlaySound 函式，簡單播放
- 多媒體音訊，PlaySound 函式
- 音訊、PlaySound 函式
- 波形音訊，PlaySound 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688688"
---
# <a name="simple-audio-playback"></a>簡易音訊播放

您可以使用下列函式，在單一函式呼叫中播放應用程式中的波形音訊。



| 函式                                                      | 描述                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | 播放對應到指定系統警示等級的音效。                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | 播放的音效與登錄中輸入的系統音效或指定檔案的內容相對應。 |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | 提供 [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 的所有功能，而且可以直接存取資源。           |



 

**MessageBeep** 函式是 WIN32 API 的標準元件;因為其功能非常有限，並記載于其他地方，所以不會在這裡討論。

列出的函式支援下列波形音訊來源：

-   波形-與系統警示等級相關聯的音訊檔案
-   由登錄中的專案所指定的波形音訊檔案
-   記憶體中的 WAVE 資源
-   波形-依名稱指定的音訊檔案

[**SndPlaySound**](/previous-versions//dd798676(v=vs.85))和 [**PlaySound**](/previous-versions//dd743680(v=vs.85))函式會將整個波形-音訊檔案載入記憶體中，而且實際上會限制它們可以播放的檔案大小。 使用 **sndPlaySound** 和 **PlaySound** 來播放很小的波形音訊檔案，最多可達100k。 這兩個函式也需要音效資料的格式，可由其中一個已安裝的波形音訊驅動程式（包括 wave 對應程式）播放。

針對較大的音效檔，請使用 Media Control 介面 (MCI) 服務。 如需詳細資訊，請參閱 [MCI](mci.md)。

 

 