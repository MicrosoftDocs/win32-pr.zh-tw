---
description: 這個範例應用程式會示範事件驅動的緩衝，使用核心音訊 Api 將音訊資料轉譯至使用者指定的輸出裝置。
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c23213e1e60d0fdf77de67a91ea3bba3c928a51f9e562876dd1a4e018595dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119216548"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的事件驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>描述

這個範例會示範下列功能。

-   適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。
-   串流管理作業的 WASAPI。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| 位置    | 路徑/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ RenderExclusiveEventDriven \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 RenderExclusiveEventDriven 範例，請使用下列步驟：

1.  開啟 Windows SDK 的 CMD shell，並變更為 RenderExclusiveEventDriven 範例目錄。
2.  在 RenderExclusiveEventDriven 目錄中執行命令 `start WASAPIRenderExclusiveEventDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPIRenderExclusiveEventDriven 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 sdk 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 sdk 組建環境。 在此情況下，除非您明確設定在專案檔 WASAPIRenderExclusiveEventDriven 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立示範應用程式，則會產生可執行檔（WASAPIRenderExclusiveEventDriven.exe）。 若要執行它，請 `WASAPIRenderExclusiveEventDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。 下列範例顯示如何在預設的多媒體裝置上指定播放持續時間來執行範例。

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

下表顯示引數。

| 引數        | 描述                                                |
|-----------------|------------------------------------------------------------|
| -?              | 顯示說明。                                                |
| -H              | 顯示說明。                                                |
| -f              | 以 Hz 為間隔的正弦波頻率。                                 |
| -l              | 音訊轉譯延遲（以毫秒為單位）。                      |
| -d              | 正弦波持續時間（以秒為單位）。                             |
| -M              | 停用 MMCSS。                                 |
| -主控台        | 使用預設的主控台裝置。                            |
| -通訊 | 使用預設通訊裝置。                      |
| -多媒體     | 使用預設的多媒體裝置。                         |
| -端點       | 使用參數值中指定的端點識別碼。 |



 

如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取轉譯會話的裝置。 當使用者指定裝置之後，應用程式會以 440 Hz 轉譯正弦波，以達10秒。 您可以藉由指定-f 和-d 參數值來修改這些值。

RenderExclusiveEventDriven 範例會示範事件驅動的緩衝。 此範例顯示如何：

-   將音訊用戶端具現化，將其設定為在獨佔模式中執行，並在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)的呼叫中設定 **AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback** 旗標，以啟用事件驅動的緩衝。
-   藉由呼叫 [**IAudioClient：： SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) 方法，將用戶端與準備好呈現的範例產生關聯。
-   建立轉譯執行緒，以處理來自音訊引擎的範例。
-   在將緩衝區傳送至裝置之前，請先在128位元組界限上適當地對齊緩衝區。 這是藉由調整引擎的週期來完成。
-   檢查裝置端點的混合格式，以判斷是否可以轉譯樣本。 如果裝置不支援混合格式，資料會轉換成 PCM。
-   處理資料流程切換。

當轉譯會話開始且資料流程開始時，音訊引擎會發出通知給用戶端的事件處理常式，以便在每次緩衝區可供用戶端處理時通知用戶端。 音訊資料也可以在計時器驅動迴圈中處理。 [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)範例會示範這個模式。

如需呈現資料流程的詳細資訊，請參閱轉譯 [資料流程](rendering-a-stream.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



