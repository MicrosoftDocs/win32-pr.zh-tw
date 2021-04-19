---
description: 這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼影像檔案，以及 Direct2D 將影像轉譯至螢幕。
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: 使用 Direct2D 範例的 WIC 影像檢視器
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106999063"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>使用 Direct2D 範例的 WIC 影像檢視器

此範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼影像檔案，並 Direct2D 以將影像轉譯至螢幕。

## <a name="requirements"></a>規格需求

此範例具有下列需求。

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows Vista |
| 最小 Windows SDK | 適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |

## <a name="downloading-the-sample"></a>下載範例

您可以在 [WIC 檢視器 D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d)取得此範例。

## <a name="building-the-sample"></a>建置範例

### <a name="using-visual-studio-preferred-method"></a>使用 Visual Studio (慣用方法) 

1. 開啟 Windows 檔案總管，巡覽至目錄。
2. 按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。
3. 在 [建置] 功能表中，選取 [建置方案]。 應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。

### <a name="using-the-command-prompt"></a>使用命令提示字元

若要使用命令提示字元建立範例：

1. 開啟 [命令提示字元] 視窗，並流覽至範例目錄。
2. 輸入 `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>執行範例

當您啟動應用程式之後，請使用 [檔案 **] 功能表的 [** **開啟**] 命令載入影像檔案。

## <a name="see-also"></a>另請參閱

[Microsoft Windows Imaging 編解碼器](-wic-lh.md)

[程式設計手冊](-wic-programming-guide.md)

[參考](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[範例和程式碼範例](-wic-samples.md)
