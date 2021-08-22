---
title: 正在抓取目前的播放位置
description: 正在抓取目前的播放位置
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- 波形音訊、目前的播放位置
- 波形-音訊介面、目前的播放位置
- 播放波形-音訊檔案，目前的播放位置
- waveOutGetPosition 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85bc46e476786625ccae51802e0b720379a935110eb37d941c4c76d69d94783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689048"
---
# <a name="retrieving-the-current-playback-position"></a>正在抓取目前的播放位置

您可以使用 [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) 函式，在聲音音訊播放時，監視檔案內目前的播放位置。

針對波形音訊裝置，範例是慣用的時間格式，用來表示目前的位置。 因此，波形音訊裝置的目前位置會指定為波形音訊檔案開頭的一個通道樣本數。 若要查詢波形音訊裝置的目前位置，請將 [**MMTIME**](/previous-versions//dd757347(v=vs.85))結構的 **wType** 成員設定為時間範例， \_ 並將此結構傳遞至 **waveOutGetPosition**。

**MMTIME** 結構可代表一或多個不同格式的時間，包括毫秒、範例、SMPTE (的運動圖片和電視工程師) ，以及 MIDI 歌曲指標格式。 **WType** 成員會指定用來代表時間的格式。 在呼叫使用 **MMTIME** 結構的函式之前，您必須先設定 **wType** ，以指出您所要求的時間格式。 請務必在呼叫之後檢查 **wType** ，以查看是否支援要求的時間格式。 如果不支援要求的時間格式，設備磁碟機會以替代時間格式指定時間，並將 **wType** 成員變更為選取的時間格式。

如需 **MMTIME** 結構的詳細資訊，請參閱 [多媒體計時器](multimedia-timers.md)。

 

 