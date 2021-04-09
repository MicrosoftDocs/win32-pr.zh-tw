---
title: 播放裝置
description: 播放裝置
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY 命令
- MCIAVI 播放視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933238"
---
# <a name="playing-a-device"></a>播放裝置

[**Play**](play.md) ([**MCI \_ play**](mci-play.md)) 命令會開始播放裝置。 如果沒有任何旗標，此命令會從目前的位置開始播放並播放，直到命令中斷或到達媒體或檔案的結尾為止。 播放之後，目前的位置是在媒體的結尾。 您也可以使用 [**搜尋**](seek.md) ([**MCI \_ 搜尋**](mci-seek.md)) 命令來變更目前的位置。

大部分支援 **play** 命令的裝置也都支援 \_ 從)  (mci，以及將 (MCI 傳送 \_ 至) 旗標。 這些旗標會指出裝置應該開始和停止播放的位置。 例如，下列命令會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式，從第一個播放軌的開頭播放 CD 音訊光碟：


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



某些裝置類型會擴充此命令，以利用特定裝置的功能。 例如， **videodisc** 裝置類型的 [**play**](play.md)命令包含「快速」 (MCI \_ VD \_ \_ 快速) 、「慢」 (mci \_ VD \_ 播放 \_ 慢) 和「掃描」 (mci \_ VD \_ play \_ 掃描) 旗標。

> [!Note]  
> 指派給位置值的單位取決於裝置所使用的時間格式。 每個裝置都有預設的時間格式，但您應該先使用 [**set**](set.md) ([**MCI \_ set**](mci-set.md)) 命令來指定時間格式，然後再發出使用位置值的任何命令。

 

## <a name="playing-an-avi-file"></a>播放 AVI 檔案

Windows 中的影片檔案是由至少兩個交錯資料流程所組成：影片 (圖形) 串流和音訊串流。 您可以使用 MCI 命令輕鬆地播放這些 (AVI) 檔案的音訊影片。 下列各節討論如何播放 AVI 檔案。

## <a name="setting-up-an-mciavi-playback-window"></a>設定 MCIAVI 播放視窗

您的應用程式可以指定下列選項，以定義播放 AVI 檔案的播放視窗：

-   使用 MCIAVI 驅動程式的預設快顯視窗。
-   指定可供 MCIAVI 驅動程式用來建立播放視窗的父視窗和視窗樣式。
-   指定 MCIAVI 驅動程式用來播放的播放視窗。
-   在全螢幕顯示上播放 AVI 檔案。

如果您的應用程式未指定任何視窗選項，MCIAVI 驅動程式會建立播放順序的預設視窗。 驅動程式會針對 [**開啟**](open.md) 的 ([**MCI \_ open**](mci-open.md)) 命令建立此播放視窗，但在您的應用程式傳送命令以顯示視窗或播放檔案之前，不會顯示視窗。 此預設播放視窗是一個快顯視窗，具有調整大小框線、標題列、寬框架、 **視窗** 功能表及最小化按鈕。

當您的應用程式發出 **open** 命令時，也可以指定父視窗控制碼和視窗樣式。 在此情況下，MCIAVI 驅動程式會根據這些規格（而不是預設的快顯視窗）來建立視窗。 您的應用程式可以指定適用于 [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數的任何視窗樣式。 需要父視窗的樣式（例如 WS 子系 \_ ）應該包含父視窗控制碼。

您的應用程式也可以建立自己的視窗，並使用 [**window**](window.md) ([**MCI \_ 視窗**](mci-window.md)) 命令，提供 MCIAVI 驅動程式的控制碼。 MCIAVI 驅動程式會使用這個視窗，而不是建立它自己的驅動程式。

當 MCIAVI 驅動程式建立播放視窗，或從您的應用程式取得視窗控制碼時，在您的應用程式播放序列或傳送命令以顯示視窗之前，不會顯示視窗。 您的應用程式可以使用 [ **視窗]** 命令來顯示視窗，而不播放順序。 例如，下列命令會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85))來顯示視窗：


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



在此範例中，「電影」是數位視訊裝置的別名。

您的應用程式也可以全螢幕播放 AVI 檔案。 若要播放全螢幕，請使用 [](play.md) 「全螢幕」 (mci MCIAVI play 全螢幕) 旗標來修改 Play ([**MCI \_ play**](mci-play.md)) 命令 \_ \_ \_ 。 當您的應用程式使用這個旗標時，MCIAVI 驅動程式會使用 320 x 240 圖元的全螢幕格式來播放序列。 例如，下列命令會使用 "movie" 作為別名) 來播放開啟的檔案全螢幕 (：


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>變更 AVI 檔案的播放狀態

您的應用程式可以使用 [**搜尋**](seek.md) ([**MCI \_ 搜尋**](mci-seek.md)) 命令將目前位置移至 AVI 檔案中的開頭、結尾或任意位置。 MCIAVI 驅動程式有兩種搜尋模式：精確且不精確。 您的應用程式可以使用 [**set**](set.md) ([**MCI \_ set**](mci-set.md)) 命令來變更搜尋模式。 當您使用 **set** 「精確搜尋」時，MCIAVI 驅動程式會精確搜尋您應用程式所指定的框架。 如果檔案暫時壓縮，而您的應用程式未指定主要畫面格，這可能會造成延遲。 當您使用 **set** "seek off" 時，MCIAVI 驅動程式會搜尋暫時壓縮檔案中最接近的主要畫面格。

有些 MCI 命令可讓您的應用程式以其他方式改變 AVI 檔案的播放。 例如，AVI 檔案預設會以正常速度播放，但您的應用程式可以使用「速度」旗標搭配 **set** 命令來增加或減少此速度。 若是 AVI 檔案，通常會有1000的速度值。 因此，若要以一半的一般速度播放電影，您的應用程式可以使用命令 **集** 「movie 速度500」;或者，它可以使用 **設定** 的 "movie speed 2000"，以其正常速度的兩倍播放序列。

[**Setaudio**](setaudio.md) ([**MCI \_ setaudio**](mci-setaudio.md)) 命令可讓您的應用程式控制 AVI 檔案的音訊部分。 您的應用程式可以在播放期間將音訊靜音，或者，如果有多個音訊串流檔案，請選取播放的音訊串流。

MCIAVI 驅動程式具有對話方塊，可控制其一些播放選項。 使用者可用的一些選項包括選取視窗導向或全螢幕播放、選取搜尋模式，以及縮放影像。 您的應用程式可以使用 [ [**設定**](configure.md) ([**MCI \_ 設定**](mci-configure.md)) ] 命令，以 MCIAVI 顯示此對話方塊。

## <a name="stream-handlers"></a>串流處理常式

AVI 檔案中的資料會被視為一連串的資料流程。 AVI 檔案通常包含音訊和影片串流，也可能有包含文字或某些其他自訂資料的自訂資料流程。 MCIAVI 驅動程式可以針對這些資料流程使用不同的處理常式。 如需自訂 AVI 檔案的詳細資訊，請參閱 [自訂檔案和資料流程處理常式](custom-file-and-stream-handlers.md)。

 

 