---
description: 示範如何使用 CreateProcess 方法來執行 Shell 動詞命令。
title: CreateProcess 動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858338"
---
# <a name="createprocess-verb-sample"></a>CreateProcess 動詞範例

示範如何使用 CreateProcess 方法來執行 Shell 動詞命令。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="description"></a>Description

CreateProcess 型動詞相依于執行可執行檔，並將命令列引數傳遞給它。 這種方法的功能不如 DropTarget 和 ExecuteCommand 方法，但它確實可以達成所需的跨進程行為。

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [CreateProcessVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **CreateProcessVerb** 專案目錄。
2.  輸入 `msbuild CreateProcessVerb.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **CreateProcessVerb** 專案目錄。
2.  按兩下 CreateProcessVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `CreateProcessVerb.exe` 。 或者，從 Windows 檔案總管按兩下 CreateProcessVerb.exe 的圖示。
3.  遵循顯示的對話方塊中的指示

 

 



