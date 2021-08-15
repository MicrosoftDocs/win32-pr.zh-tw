---
description: 示範如何使用 DropTarget 方法來執行 Shell 動詞。
title: DropTarget 動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ae9ae3edb2d993f2e42a2556899d45cb3b10722fc7d7a9dc5e9786560fc3078f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719530"
---
# <a name="droptarget-verb-sample"></a>DropTarget 動詞範例

示範如何使用 DropTarget 方法來執行 Shell 動詞。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="description"></a>Description

這個範例示範如何使用 DropTarget 方法來執行 Shell 動詞命令。 這是必須在 Windows XP 上運作的動詞執行的慣用方法。 此範例會將獨立本機伺服器元件物件模型 (COM) 物件中，但必須將動詞執行整合至現有的應用程式。 若要這樣做，您的主要應用程式物件會自行註冊 class factory。 該物件會針對您的應用程式動詞來實行 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。 請注意，如果您的應用程式尚未執行，COM 會啟動應用程式，但如果有的話，則會連接到應用程式的執行中實例。

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [DropTargetVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **DropTargetVerb** 專案目錄。
2.  輸入 `msbuild DropTargetVerb.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **DropTargetVerb** 專案目錄。
2.  按兩下 DropTargetVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `DropTargetVerb.exe` 。 或者，從 Windows 檔案總管按兩下 DropTargetVerb.exe 的圖示。
3.  遵循顯示的對話方塊中的指示

 

 
