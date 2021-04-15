---
description: 這個範例應用程式會使用核心音訊 Api 來變更裝置的音量（由使用者所指定）。
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468332"
---
# <a name="endpointvolume"></a>EndpointVolume

這個範例應用程式會使用核心音訊 Api 來變更裝置的音量（由使用者所指定）。

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
-   [ENDPOINTVOLUME API](endpointvolume-api.md) 來控制裝置端點的音量層級。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location    | 路徑/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ EndpointVolume \\ .。。 |



 

## <a name="building-the-sample"></a>建立範例

若要建立 x 範例，請使用下列步驟：

若要建立 EndpointVolumeChanger 範例，請使用下列步驟：

1.  開啟 Windows SDK 的 CMD shell，並變更為 EndpointVolume 範例目錄。
2.  在 EndpointVolume 目錄中執行命令 `start EndpointVolumeChanger.sln` ，以在 Visual Studio 視窗中開啟 EndpointVolumeChanger 專案。
3.  從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。 如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。 在此情況下，除非您明確設定在專案檔 WASAPIEndpointVolume 中使用的環境變數 MSSdk，否則此範例不會建立。

## <a name="running-the-sample"></a>執行範例

如果您成功建立示範應用程式，則會產生可執行檔（EndpointVolumeChanger.exe）。 若要執行它，請 `EndpointVolumeChanger` 在命令視窗中輸入，後面接著必要或選擇性的引數。 下列範例顯示如何切換預設主控台裝置上的靜音設定。

`EndpointVolumeChanger.exe -console -m`

下表顯示引數。

| 引數        | 描述                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | 顯示說明。                                                         |
| -H              | 顯示說明。                                                         |
| -+              | 將音訊端點裝置上的音量層級遞增一個步驟。 . |
| -up             | 將音訊端點裝置上的音量層級遞增一個步驟。   |
| --              | 將音訊端點裝置上的音量層級減少一個步驟。   |
| -down           | 將音訊端點裝置上的音量層級減少一個步驟。   |
| -v              | 設定音訊端點裝置上的主要磁碟區層級。          |
| -主控台        | 使用預設的主控台裝置。                                     |
| -通訊 | 使用預設通訊裝置。                               |
| -多媒體     | 使用預設的多媒體裝置。                                  |
| -端點       | 使用參數值中指定的端點識別碼。          |



 

如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取裝置。 當使用者指定裝置之後，應用程式會顯示端點目前的磁片區設定。 您可以使用上表所述的參數來控制該磁片區。

如需控制音訊端點裝置音量層級的詳細資訊，請參閱 [ENDPOINTVOLUME API](endpointvolume-api.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用核心音訊 Api 的 SDK 範例](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



