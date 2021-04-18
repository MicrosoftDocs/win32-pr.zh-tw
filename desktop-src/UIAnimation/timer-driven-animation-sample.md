---
title: Timer-Driven 的動畫範例
description: 顯示如何使用 Windows 動畫搭配動畫計時器，同時使用 GDI + 以動畫顯示視窗的背景色彩。
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314584"
---
# <a name="timer-driven-animation-sample"></a>Timer-Driven 的動畫範例

顯示如何使用 Windows 動畫搭配動畫計時器，同時使用 GDI + 以動畫顯示視窗的背景色彩。

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

1.  開啟 [命令提示字元] 視窗，並流覽至 TimerDriven 專案目錄。 例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ TimerDriven。

2.  執行下列命令： **Msbuild TimerDriven .sln**

**若要使用 Microsoft Visual Studio (慣用的來建立範例)**

1.  開啟 Windows 檔案總管，然後流覽至 TimerDriven 專案目錄。

2.  按兩下 TimerDriven .sln 檔案的圖示，在 Visual Studio 中開啟專案。

    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

若要執行範例：

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。

2.  在命令提示字元中執行 **TimerDriven.exe** ，或按兩下 Windows 檔案總管中 TimerDriven.exe 的圖示。

3.  按一下工作區中的任何位置，視窗的背景色彩會變更為隨機色彩。

 

 




