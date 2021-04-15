---
description: 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468328"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [查看範例檔案](#view-the-sample-files)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

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



| Location    | 路徑/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ RenderExclusiveTimerDriven \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 RenderExclusiveTimerDriven 範例，請使用下列步驟：

1.  開啟 Windows SDK 的 CMD shell，並變更為 RenderExclusiveTimerDriven 範例目錄。
2.  在 RenderExclusiveTimerDriven 目錄中執行命令 `start WASAPIRenderExclusiveTimerDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPIRenderExclusiveTimerDriven 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。 在此情況下，除非您明確設定在專案檔 WASAPIRenderExclusiveTimerDriven 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="view-the-sample-files"></a>查看範例檔案

如果您成功建立示範應用程式，則會產生可執行檔（WASAPIRenderExclusiveTimerDriven.exe）。 若要執行它，請 `WASAPIRenderExclusiveTimerDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。 下列範例顯示如何在預設主控台裝置上指定播放持續時間來執行範例。

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

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

RenderExclusiveTimerDriven 示範計時器驅動的緩衝。 在此模式中，用戶端必須等待一段時間， (-d 參數值所指定的時間長度（以毫秒為單位）) 。 當用戶端喚醒時，會從引擎提取下一組範例。 在緩衝迴圈中的每個處理階段之前，用戶端必須找出要轉譯的資料量，讓資料不會溢出緩衝區。

要在指定的裝置上播放的音訊資料，可透過啟用事件驅動的緩衝處理來處理。 RenderExclusiveTimerDriven 範例會示範這個模式。

如需呈現資料流程的詳細資訊，請參閱轉譯 [資料流程](rendering-a-stream.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



