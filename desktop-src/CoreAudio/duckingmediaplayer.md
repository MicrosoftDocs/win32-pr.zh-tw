---
description: 這個範例應用程式會藉由執行媒體播放程式來示範串流衰減，以顯示系統提供的預設衰減行為、退出回避事件，以及在收到回避事件時執行自訂處理。
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab5a469ec2a7fb1551980d0a08a758e8e8e8f522831dc2148b2d8fb222ecdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828279"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

這個範例應用程式會藉由執行媒體播放程式來示範串流衰減，以顯示系統提供的預設衰減行為、退出回避事件，以及在收到回避事件時執行自訂處理。 此範例必須在 conjuction with [DuckingCaptureSample](duckingcapturesample.md)中使用。 如需回避或串流衰減的詳細資訊，請參閱 [預設回避體驗](stream-attenuation.md)。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>描述

這個範例會示範下列功能。

-   DirectShow 播放媒體檔案。
-   串流管理和處理回避事件的[WASAPI](wasapi.md) 。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location    | 路徑/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ DuckingMediaPlayer \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 DuckingMediaPlayer 範例，請使用下列步驟：

1.  在 Visual Studio 2008 中開啟 DuckingMediaPlayer .sln。
2.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 sdk 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 sdk 組建環境。 在此情況下，除非您明確設定在專案檔 DuckingMediaPlayer 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立應用程式，則會產生可執行檔（DuckingMediaPlayer.exe）。 若要執行它，請選取 [ **開始調試** ] 或 [ **啟動但不進行調試** ] **，或** `DuckingMediaPlayer` 在命令視窗中輸入。

若要觀看回避的示範，您必須同時執行 DuckingMediaPlayer 和 DuckingCaptureSample。 DuckingCaptureSample 會開啟通訊資料流程，並通知系統產生回避事件。 當回避事件發生時，系統會通知 DuckingMediaPlayer，而 media player 會執行使用者所要求的動作。

若要停用回避行為：

1.  在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。
2.  在 DuckingMediaPlayer 上，選取要播放的媒體檔案，並將回避選項指定為 **退出回避**。

請注意，媒體檔案會播放，而不會發生任何中斷。 系統會忽略開啟的通訊資料流程時，系統所產生的事件。

若要示範系統提供的預設回避行為，請執行下列動作：

1.  從 [控制台] 選取 [音效 **] 選項。** 在 [ **通訊** ] 索引標籤上，選取 [ **將其他音效的音量減少 80%**]。
2.  在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。
3.  在 DuckingMediaPlayer 上，選取要播放的媒體檔案，而不選擇任何回避選項。
4.  在 [DuckingCaptureSample] 視窗中，按一下 [ **停止** ] 以停止通訊串流。

請注意，當 DuckingCaptureSample 開啟通訊串流時，DuckingMediaPlayer 播放的媒體檔案不會中斷，但音量層級會降低。 當通訊會話停止時，磁片區會重設為原始設定。 此資料流程衰減行為是系統所執行的預設回避行為。

若要查看媒體播放機所實行的自訂回避行為：

1.  在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。
2.  在 DuckingMediaPlayer 上，選取要播放的媒體檔案，然後將回避選項指定為 [ **暫停**]。
3.  在 [DuckingCaptureSample] 視窗中，按一下 [ **停止** ] 以停止通訊串流。

請注意，當 DuckingCaptureSample 開啟通訊串流時，DuckingMediaPlayer 所播放的媒體檔案會暫停。 停止通訊會話時，就會繼續播放。 此資料流程衰減行為是媒體播放機所執行的回避行為。

DuckingMediaPlayer 也會示範如何將每個應用程式的音量控制項與磁片區混音器整合。

如需有關資料流程衰減功能的詳細資訊，請參閱 [預設回避體驗](stream-attenuation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



