---
description: 這個範例會示範如何解碼 GIF 檔案中的各種框架、為每個框架讀取適當的中繼資料、撰寫框架，以及使用 Direct2D 呈現動畫。
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: WIC 動畫 Gif 範例
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "107000646"
---
# <a name="wic-animated-gif-sample"></a>WIC 動畫 GIF 範例

這個範例會示範如何解碼 GIF 檔案中的各種框架、為每個框架讀取適當的中繼資料、撰寫框架，以及使用 Direct2D 呈現動畫。

## <a name="requirements"></a>規格需求

此範例具有下列需求。

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 7 |
| 最小 Windows SDK | 適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [WIC 動畫 GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)中取得。

## <a name="building-the-sample"></a>建置範例

### <a name="using-visual-studio-preferred-method"></a>使用 Visual Studio (慣用方法) 

1. 開啟 Windows 檔案總管，巡覽至目錄。
2. 按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。
3. 在 [建置] 功能表中，選取 [建置方案]。 應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。

### <a name="using-the-command-prompt"></a>使用命令提示字元

使用命令提示字元建立範例。

1. 開啟命令提示字元，然後流覽至範例目錄。
2. 輸入 `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>執行範例

應用程式啟動之後，使用 [檔案 **] 功能表的 [** **開啟**] 命令載入影像檔案。 支援視窗調整大小。

## <a name="see-also"></a>另請參閱

[Microsoft Windows Imaging 編解碼器](-wic-lh.md)

[程式設計手冊](-wic-programming-guide.md)

[參考](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[範例和程式碼範例](-wic-samples.md)
