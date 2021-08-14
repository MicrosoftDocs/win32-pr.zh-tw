---
description: 示範如何使用 ExecuteCommand 方法來執行 Shell 動詞。
title: 執行命令動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e32b472d63b9d2d779c97b64833f354e7d4d2eaed034d3a213ae4e101f7beb3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858267"
---
# <a name="execute-command-verb-sample"></a>執行命令動詞範例

示範如何使用 ExecuteCommand 方法來執行 Shell 動詞。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="description"></a>Description

這是動詞命令的慣用方法，因為它提供最大的彈性、很簡單，而且支援跨進程啟用。 這個範例會將獨立的本機伺服器元件物件模型 (COM) 物件中，但必須將動詞執行整合到現有的應用程式中。 若要這樣做，您的主要應用程式物件必須自行註冊 class factory。 該物件會針對您的應用程式動詞來實行 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。 請注意，如果您的應用程式尚未執行，COM 會啟動應用程式，但如果有的話，則會連接到應用程式的執行中實例。

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExecuteCommandVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **ExecuteCommandVerb** 專案目錄。
2.  輸入 `msbuild ExecuteCommand.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **ExecuteCommandVerb** 專案目錄。
2.  按兩下 ExecuteCommand .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `ExecuteCommand.exe` 。 或者，從 Windows 檔案總管按兩下 ExecuteCommand.exe 的圖示。
3.  遵循顯示的對話方塊中的指示

 

 
