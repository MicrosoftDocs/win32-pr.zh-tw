---
description: 這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範事件驅動的緩衝。
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110789"
---
# <a name="capturesharedeventdriven"></a>CaptureSharedEventDriven

這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範事件驅動的緩衝。

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
-   串流管理作業的[WASAPI](wasapi.md) ，例如啟動和停止資料流程，以及串流切換。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location    | 路徑/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ CaptureSharedEventDriven \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 CaptureSharedEventDriven 範例，請使用下列步驟：

1.  開啟 Windows SDK 的 CMD shell，並變更為 CaptureSharedEventDriven 範例目錄。
2.  在 CaptureSharedEventDriven 目錄中執行命令 `start WASAPICaptureSharedEventDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPICaptureSharedEventDriven 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。 在此情況下，除非您明確設定在專案檔 WASAPICaptureSharedEventDriven 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立示範應用程式，則會產生可執行檔（WASAPICaptureSharedEventDriven.exe）。 若要執行它，請 `WASAPICaptureSharedEventDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。 下列範例顯示如何在預設的多媒體裝置上指定捕捉持續時間來執行範例。

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

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

CaptureSharedEventDriven 示範事件驅動的緩衝。 針對此範例具現化的音訊用戶端設定為在共用模式中執行，而用戶端的音訊緩衝區處理是由在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)的呼叫中設定 **AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback** 旗標，使事件成為驅動。 此範例會顯示用戶端如何藉由呼叫 [**IAudioClient：： SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) 方法，提供事件控制碼給系統。 當 capture 會話開始且資料流程開始時，音訊引擎會發出通知給用戶端的事件處理常式，每次緩衝區準備好供用戶端處理時使用。 音訊資料也可以在計時器驅動迴圈中處理。 這是在 [CaptureSharedTimerDriven](capturesharedtimerdriven.md) 範例中 demostrated 的模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



