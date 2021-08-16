---
title: PlaySound 函式
description: PlaySound 函式
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- 多媒體音訊，PlaySound 函式
- 音訊、PlaySound 函式
- 波形音訊，PlaySound 函式
- PlaySound 函式，關於
- sndPlaySound 函式
- PlaySound 函式，相較于 sndPlaySound 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370848"
---
# <a name="the-playsound-function"></a>PlaySound 函式

如果音效符合可用記憶體，您可以使用 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 函式來播放波形音訊。  ([**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式會提供 PlaySound 功能的子集。 若要最大化 Win32 應用程式的可攜性，請使用 **PlaySound**，而不是 **sndPlaySound**。 ) 

**PlaySound** 函數可讓您以下列三種方式之一來指定音效：

-   作為系統警示，使用儲存在 WIN.INI 檔案或登錄中的別名
-   作為檔案名
-   作為資源識別碼

[**PlaySound**](/previous-versions//dd743680(v=vs.85))函式可讓您在連續迴圈中播放音效，只有當您再次呼叫 **PlaySound** 時，才會結束，指定 *pszSound* 參數的另一個音效的 **Null** 或音效識別碼。

您可以使用 **PlaySound** 以同步或非同步方式播放音效，並以其他方式控制函式的行為（當它必須共用系統資源時）。

如需有關使用 PlaySound 的詳細資訊，請參閱下列主題：

-   [使用 PlaySound 來播放 Waveform-Audio 檔案](using-playsound-to-play-waveform-audio-files.md)
-   [使用 PlaySound 來迴圈聲音](using-playsound-to-loop-sounds.md)
-   [使用 PlaySound 來播放系統音效](using-playsound-to-play-system-sounds.md)

如需有關如何在 Win32 應用程式中使用 **PlaySound** 的更多範例，請參閱 [播放 WAVE 資源](playing-wave-resources.md)。

 

 