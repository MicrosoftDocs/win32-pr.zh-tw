---
description: 此範例會使用核心音訊 Api 來捕捉高品質的語音串流。 此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用由 Microsoft 所提供的 AEC （也稱為語音捕獲 DSP）。
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111561"
---
# <a name="aecmicarray"></a>AECMicArray

此範例會使用核心音訊 Api 來捕捉高品質的語音串流。 此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用由 Microsoft 所提供的 AEC （也稱為語音捕獲 DSP）。

本主題將包含以下各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例會示範下列功能。

-   [MMDevice](mmdevice-api.md) 多媒體裝置的列舉和選取。
-   串流管理作業的[WASAPI](wasapi.md) ，例如啟動和停止資料流程、串流切換。
-   用於列舉音訊介面卡的[DeviceTopology](devicetopology-api.md) 。
-   [EndpointVolume](endpointvolume-api.md) 控制 [音訊會話](audio-sessions.md)的音量層級。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本                     |
|----------------------------------------------------------------|-----------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista 或更新版本      |
| Visual Studio                                                  | 2005 (非 express 版本)  |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location    | 路徑/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ AECMicArray \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 AecSDKDemo 範例，請使用下列步驟：

1.  開啟 [SDK 命令] 視窗。
2.  輸入 **cd% MSSDK% \\ 安裝程式**。
3.  執行 VCIntegrate.exe。

    從這裡開始，命令視窗會有適當的環境設定，以建立利用 SDK 的應用程式。

4.  建置範例。

## <a name="running-the-sample"></a>執行範例

如果您成功建立示範應用程式，則會產生可執行檔 AecSDKDemo.exe。 若要執行它，請 `AecSDKDemo` 在命令視窗中輸入，後面接著必要或選擇性的引數，如下所述。

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

下表顯示引數。

| 引數  | 描述                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | 必要。 指定輸出檔名稱。                                                                                                 |
| -mod      | 必要。 指定語音捕獲系統模式。 如需詳細資訊，請參閱範例讀我檔案中的「設定 voice capture」一節。 |
| -特徵     | 選擇性。 開啟 (1) 或 off (0) 的功能模式。                                                                                       |
| -ns       | 選擇性。 開啟 (1) 或 off (0) 的雜訊抑制。 您必須開啟功能模式，才能指定此功能。                                     |
| -agc      | 選擇性。 開啟 (1) 或 off (0) 的數位 AGC。 您必須開啟功能模式，才能指定此功能。                                           |
| -cntrclip | 選擇性。 在 (1) 或 off (0) 上開啟中央剪輯。 您必須開啟功能模式，才能指定此功能。                                       |
| -spkdev   | 選擇性。 指定喇叭裝置索引。 如果未指定，系統會要求使用者選取。                                         |
| -micdev   | 選擇性。 指定麥克風裝置索引。 如果未指定，系統會要求使用者選取。                                      |
| -持續時間 | 選擇性。 指定應用程式執行的時間長度。                                                                                    |



 

這個範例應用程式不會播放任何信號。 若要適當地執行適用于 AEC 的模式 (模式0和 4) ，使用者必須透過指定給 SQL-DMO 的相同喇叭裝置來播放某些音訊信號 (也就是由 "-spkdev" 選項指定的裝置) ，它會在雙向交談案例中模擬最遠的聲音。 使用者可以使用任何玩家來播放任何音訊信號。 如果選取的喇叭裝置上沒有作用中的轉譯資料流程，則將無法處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



