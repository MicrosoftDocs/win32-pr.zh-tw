---
title: 定義播放範圍
description: 定義播放範圍
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom 宏
- MCIWndPlayTo 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853c74cc4115cee72e4253e339f934e73b8d8e7e223f1b91e9992969c4ce3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785418"
---
# <a name="defining-playback-scope"></a>定義播放範圍

MCIWnd 提供可讓您定義播放 *範圍* 的宏。 範圍是您想要播放播放的部分。 例如，您可以使用 [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) 宏，從開始位置以外的位置播放內容。 此宏會移至指定的位置、開始播放，然後繼續至內容的結尾。 同樣地，您可以使用 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏來播放內容到指定的結束點。 這個宏會從目前的播放位置開始播放，直到到達指定的位置或到達內容的結尾為止（以先達到者為准）。

此外，您也可以使用 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) 宏來定義開始和結束位置。 這個宏會移至指定的開始位置並播放，直到到達指定的結束位置或內容結尾為止。

 

 




