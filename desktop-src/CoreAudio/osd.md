---
description: 此範例會使用核心音訊 Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077512"
---
# <a name="osd"></a>OSD

此範例會使用核心音訊 Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。 當使用者調整 Windows 音量控制程式中的音量層級時，畫面上顯示畫面會顯示 Sndvol.exe，而且在短時間內，磁片區層級會維持不變。

本主題將包含以下各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>描述

這個範例會示範下列功能。

-   適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。
-   音訊 [ENDPOINTVOLUME API](endpointvolume-api.md)

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista 或更新版本 |
| Visual Studio                                                  | 2005或更新版本          |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| 位置    | 路徑/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ OSD \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

1.  開啟 Windows SDK 的 CMD shell，並變更為 OSD 範例目錄。
2.  在 osd 目錄中執行 "start .osd" 命令，以在 Visual Studio 視窗中開啟 osd 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 sdk 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 sdk 組建環境。 在此情況下，除非您明確設定用於專案檔 vcproj 的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

1.  在 Windows Vista 或更新版本中執行 OSD 可執行檔 OSD.exe。 請注意，您不會看到應用程式的系統匣圖示或視窗，但您可以使用 TaskMgr.exe 查看正在執行的進程。
2.  執行 sndvol.exe 來變更音量或靜音，或使用鍵盤控制項或隱藏控制項來變更音量。 OSD 使用者介面隨即顯示。
3.  若要結束應用程式，請執行 TaskMgr.exe、反白顯示 OSD.exe 進程，然後按一下 [ **結束處理** 程式]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



