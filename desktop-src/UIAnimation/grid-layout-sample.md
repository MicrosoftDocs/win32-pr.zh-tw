---
title: 方格版面配置範例
description: 示範如何使用 Direct2D 以動畫顯示影像的方格，以使用 Windows 動畫。
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "103681622"
---
# <a name="grid-layout-sample"></a>方格版面配置範例

示範如何使用 Direct2D 以動畫顯示影像的方格，以使用 Windows 動畫。

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location                               | 路徑/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows 軟體開發套件7。0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Code Gallery (程式碼庫)                           | [Windows 動畫管理員範例程式碼](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。 例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。

## <a name="building-the-sample"></a>建立範例

您可以使用下列其中一種方法來建立範例。

**若要在命令提示字元中建立範例**

1.  開啟 [命令提示字元] 視窗，並流覽至 GridLayout 專案目錄。 例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ GridLayout

2.  執行下列命令： **Msbuild GridLayout .sln**

**若要使用 Microsoft Visual Studio (慣用的來建立範例)**

1.  開啟 Windows 檔案總管，然後流覽至 GridLayout 專案目錄。

    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

2.  按兩下 GridLayout .sln 檔案的圖示，在 Visual Studio 中開啟專案。

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

若要執行範例：

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。

2.  在命令提示字元中執行 **GridLayout.exe** ，或按兩下 Windows 檔案總管中 GridLayout.exe 的圖示。

3.  從圖片庫載入範例影像。 調整視窗的大小，影像會在方格中排列。

 

 




