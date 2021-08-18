---
description: 這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76515f9d20e31bf4583b715e09da38c29bfdac34f6c975087f64bf2617696542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018456"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。 此應用程式會執行聊天用戶端，此用戶端會使用核心音訊 Api 從通訊裝置讀取音訊資料，並在輸出裝置上播放。

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
-   用來存取通訊捕捉和轉譯裝置、串流管理作業，以及處理回避事件的[WASAPI](wasapi.md) 。
-   用於存取通訊裝置和捕獲音訊輸入的[WAVE api](/previous-versions//ms713499(v=vs.85)) 。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| 位置    | 路徑/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ DuckingCaptureSample \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 DuckingCaptureSample 範例，請使用下列步驟：

1.  在 Visual Studio 2008 中開啟 DuckingCaptureSample .sln。
2.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 sdk 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 sdk 組建環境。 在此情況下，除非您明確設定在專案檔 DuckingCaptureSample 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立應用程式，則會產生可執行檔（DuckingCaptureSample.exe）。 若要執行它，請選取 [ **開始調試** ] 或 [ **啟動但不進行調試** ] **，或** `DuckingCaptureSample` 在命令視窗中輸入。

DuckingCaptureSample 會為使用者提供兩個從預設主控台裝置（WASAPI 和 Wave Api）捕獲音訊的實施。 若要啟動捕獲會話，請選取模式，然後按一下應用程式使用者介面上的 [ **啟動** ]。 若要結束會話，請按一下 [ **停止**]。 根據使用者指定 (輸入或輸出) 的裝置，應用程式會使用 MMDevice API 來取得預設轉譯或捕捉通訊裝置的參考。 當使用者啟動聊天會話之後，應用程式會執行下列工作：

-   在事件驅動模式中建立並初始化音訊用戶端。
-   將用戶端與事件處理常式產生關聯，該控制碼表示範例已準備好進行捕捉或轉譯。
-   設定傳輸的捕獲用戶端和轉譯用戶端。
-   建立聊天線程，並啟動音訊引擎。

為了捕獲音訊資料，在每次處理階段中，此範例會使用 capture 用戶端來取得緩衝區中可用的已捕獲資料量、從預設輸入裝置讀取資料，以及釋出封包，並讓緩衝區可用來讀取下一組已捕獲的資料。

針對轉譯，應用程式會決定已排入佇列以在 capture 端點緩衝區中播放的資料量。 它會視情況寫入緩衝區，並釋出緩衝區，以準備下一次處理行程，直到所有資料都已寫入為止。 若是轉譯，則會 prerolled 無訊息框架，以防止音訊引擎在啟動時瑕疵。 DuckingCaptureSample 也會顯示如何從磁片區混音器隱藏轉譯資料流程。

如需資料流程衰減功能的詳細資訊，請參閱 [使用通訊裝置](using-the-communication-device.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
