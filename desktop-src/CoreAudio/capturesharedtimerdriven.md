---
description: 這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範計時器驅動的緩衝。
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025932"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範計時器驅動的緩衝。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例會示範下列功能。

-   適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。
-   串流管理作業的[WASAPI](wasapi.md) 。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location    | 路徑/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ CaptureSharedTimerDriven \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 CaptureSharedTimerDriven 範例，請使用下列步驟：

1.  開啟 Windows SDK 的 CMD shell，並變更為 CaptureSharedTimerDriven 範例目錄。
2.  在 CaptureSharedTimerDriven 目錄中執行命令 `start WASAPICaptureSharedTimerDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPICaptureSharedTimerDriven 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。 在此情況下，除非您明確設定在專案檔 WASAPICaptureSharedTimerDriven 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立示範應用程式，則會產生可執行檔（WASAPICaptureSharedTimerDriven.exe）。 若要執行它，請 `WASAPICaptureSharedTimerDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。 下列範例顯示如何在預設的多媒體裝置上指定捕捉持續時間來執行範例。

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

下表顯示引數。

| 引數        | 描述                                                |
|-----------------|------------------------------------------------------------|
| -?              | 顯示說明。                                                |
| -H              | 顯示說明。                                                |
| -l              | 音訊捕獲延遲（以毫秒為單位）。                     |
| -d              | 音訊捕獲持續時間（秒）。                         |
| -M              | 停用 MMCSS。                                 |
| -主控台        | 使用預設的主控台裝置。                            |
| -通訊 | 使用預設通訊裝置。                      |
| -多媒體     | 使用預設的多媒體裝置。                         |
| -端點       | 使用參數值中指定的端點識別碼。 |



 

如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取要用於捕獲會話的裝置。 預設的主控台、通訊和多媒體裝置會列出，後面接著 [裝置] 和 [端點識別碼]。 如果未指定持續時間，則會從指定的裝置捕獲音訊串流10秒。 應用程式會將已捕捉的資料寫入至唯一命名的 .wav 檔。

CaptureSharedTimerDriven 示範計時器驅動的緩衝。 在此模式中，用戶端必須等待一段時間， (-d 參數值所指定的時間長度（以毫秒為單位）) 。 當用戶端喚醒時，會從引擎提取下一組範例。 用戶端必須先找出可用的捕獲資料量，讓資料不會溢出擷取緩衝區，才能在每次處理的緩衝迴圈中傳遞。 您可以藉由啟用事件驅動的緩衝處理，來處理從指定的裝置所捕捉的音訊資料。 [CaptureSharedEventDriven](capturesharedeventdriven.md)範例會示範這個模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



