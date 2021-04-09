---
description: 裝置角色
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: 裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110785"
---
# <a name="device-roles"></a>裝置角色

如果系統包含兩個以上的音訊轉譯端點裝置，則一部裝置最適合用來播放一種音訊內容，而另一部裝置可能最適合用來播放另一種類型的內容。 例如，如果系統有兩個轉譯裝置，則使用者可能會選擇在一部裝置上播放音樂，並在另一部裝置上播放系統通知聲音。

同樣地，如果系統包含兩個或多個音訊捕獲端點裝置，則一部裝置最適合用來捕捉一種類型的音訊內容，而另一部裝置可能最適合用來捕捉另一種類型的內容。 例如，如果系統有兩部捕獲裝置，則使用者可能會選擇在一部裝置上錄製即時音樂，以及使用其他裝置來進行語音命令。

裝置可以有三個角色：主控台、通訊和多媒體。下表說明 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉中的三個常數（EConsole、ECommunications 和 eMultimedia）所識別的裝置角色。



| ERole 常數  | 裝置角色                              | 轉譯範例             | Capture 範例                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| eConsole        | 與電腦的互動            | 遊戲和系統通知 | 語音命令                     |
| eCommunications | 與其他人交流語音 | 聊天與 VoIP                  | 聊天與 VoIP                      |
| eMultimedia     | 播放或錄製音訊內容       | 音樂和電影               | 旁白和即時音樂錄製 |



 

特定的轉譯或捕獲裝置可能指派給上表中的「無」、「一個」、「部分」或「所有」角色。 在任何時候，資料表中的每個角色都會指派給一個 (，只有一個) 轉譯裝置和一個 (，而只有一個) capture 裝置。 亦即，將角色指派給轉譯裝置的方式，與用來捕獲裝置的角色指派無關。

應用程式可能會選擇透過單一轉譯端點裝置來播放其所有輸出資料流程，並從單一的捕獲端點裝置記錄其所有輸入資料流程。 或者，應用程式可能會選擇透過一個轉譯裝置來播放其輸出資料流程，並透過其他轉譯裝置播放其他輸出資料流程。 同樣地，它可能會選擇透過一個捕獲裝置來記錄部分輸入資料流程，並透過其他捕獲裝置來記錄其他輸入資料流程。 在所有情況下，應用程式可以將每個串流指派給其角色最適合該串流的裝置。

例如，VoIP 應用程式可能會將包含環形通知的輸出資料流程，指派給呈現端點裝置（具有 eConsole 角色）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> <dt>

[使用裝置角色](device-roles-in-windows-vista.md)
</dt> <dt>

[與舊版音訊 Api 的互通性](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



