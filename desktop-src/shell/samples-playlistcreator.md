---
description: 示範如何建立在選取的 Shell 專案或容器上操作的動詞，以建立播放清單。
title: 播放清單建立者範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973833"
---
# <a name="playlist-creator-sample"></a>播放清單建立者範例

示範如何建立在選取的 Shell 專案或容器上操作的動詞，以建立播放清單。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [PlaylistCreator 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **PlaylistCreator** 專案目錄。
2.  輸入 `msbuild PlaylistCreator.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

> [!Note]  
> 如果無法使用完整的 Visual Studio，此範例也可以搭配 Visual C++ Express 版本使用。

 

1.  開啟 Windows 檔案總管，然後流覽至 **PlaylistCreator** 專案目錄。
2.  按兩下 PlaylistCreator .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。
    > [!Note]  
    > 如果您要使用 Visual C++ Express Edition 編譯64位，您必須使用 Windows SDK 提供的 x64 跨編譯器。

     

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `PlaylistCreator.exe` 。 或者，從 Windows 檔案總管按兩下 PlaylistCreator.exe 的圖示。
3.  在 Windows 檔案總管中，以滑鼠右鍵按一下包含音樂檔案的任何音樂檔或資料夾，以建立播放清單來顯示內容功能表
4.  您可以建立 m3u 或. .wpl 播放清單。 播放清單會在資料夾中建立 `%userprofile%\Music\Playlists` 。
    > [!Note]  
    > 在內容功能表中，您可以在 [ **音樂** ] 資料夾、音樂堆疊、 **音樂媒體** 櫃中的堆疊，以及音樂檔案的集合中找到新的動詞命令。

     

 

 



