---
description: 示範如何使用 ExplorerCommand 和 ExplorerCommandState 方法來執行 Shell 動詞命令。
title: Explorer 命令動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852188"
---
# <a name="explorer-command-verb-sample"></a>Explorer 命令動詞範例

示範如何使用 ExplorerCommand 和 ExplorerCommandState 方法來執行 Shell 動詞命令。

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
| GitHub  | [ExplorerCommandVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **ExplorerCommandVerb** 專案目錄。
2.  輸入 `msbuild ExplorerCommandVerb.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **ExplorerCommandVerb** 專案目錄。
2.  按兩下 ExplorerCommandVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含 ExplorerCommandVerb.dll 的目錄。 請確定您在64位的 Windows 上使用64位的 DLL 檔案。
2.  在命令列中，輸入 `regsvr32.exe ExplorerCommandVerb.dll` 。
3.  當您以滑鼠右鍵按一下 .txt 檔案時，內容功能表上會顯示兩個新的動詞命令。

 

 



