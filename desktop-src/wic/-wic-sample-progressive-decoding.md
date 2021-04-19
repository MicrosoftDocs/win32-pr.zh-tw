---
description: 這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼以漸進式層級編碼的影像。
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: WIC 漸進解碼範例
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106997436"
---
# <a name="wic-progressive-decoding-sample"></a>WIC 漸進解碼範例

這個範例示範如何使用 Windows 影像處理元件 (WIC) 來解碼以漸進式層級編碼的影像。 這個範例會使用 Direct2D，將不同的漸進層級轉譯至螢幕。

## <a name="requirements"></a>規格需求

此範例具有下列需求。

| 需求 | 值 |
|-|
| 最低支援的用戶端 | Windows 7 |
| 最小 Windows SDK | 適用于 Windows 7 的[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [WIC 漸進編碼](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding)中取得。

## <a name="building-the-sample"></a>建置範例

### <a name="using-visual-studio-preferred-method"></a>使用 Visual Studio (慣用方法) 

1. 開啟 Windows 檔案總管，巡覽至目錄。
2. 按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟檔案。
3. 在 [建置] 功能表中，選取 [建置方案]。 應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。

### <a name="using-the-command-prompt"></a>使用命令提示字元

使用命令提示字元建立範例。

1. 開啟命令提示字元，然後流覽至範例目錄。
2. 輸入 `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>執行範例

應用程式啟動之後，透過 [開啟] 功能表載入影像檔案。 載入時，預設漸進式層級會設定為0。 您可以透過功能表或向上/向下鍵來流覽至不同的漸進式層級。 目前的漸進式層級文字會顯示在主視窗狀態列上。 支援視窗調整大小。

> [!NOTE]
> 漸進式解碼只適用于已逐漸編碼的影像。 此範例所提供的映射已逐漸編碼。

## <a name="see-also"></a>另請參閱

[Microsoft Windows Imaging 編解碼器](-wic-lh.md)

[程式設計手冊](-wic-programming-guide.md)

[參考](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[範例和程式碼範例](-wic-samples.md)

[漸進式解碼總覽](-wic-progressive-decoding.md)
