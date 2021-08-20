---
description: 示範如何建立可在 Shell 專案和容器上操作的動詞，以播放專案或將專案加入至佇列。
title: 播放程式動詞命令範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a338bef9e06a7d5f4f17afad48037b95b8f1883cf60debadc0a4c5e3f2e34e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677426"
---
# <a name="player-verb-sample"></a>播放程式動詞命令範例

示範如何建立可在 Shell 專案和容器上操作的動詞，以播放專案或將專案加入至佇列。 此範例對於媒體應用程式特別有用。

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

| 位置      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [PlayerVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **PlayerVerbSample** 專案目錄。
2.  輸入 `msbuild PlayerVerbSample.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **PlayerVerbSample** 專案目錄。
2.  按兩下 PlayerVerbSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `PlayerVerbSample.exe` 。 或者，從 Windows 檔案總管按兩下 PlayerVerbSample.exe 的圖示。
3.  `Register Verbs`在 [**播放玩家動詞範例**] 對話方塊中選取。
4.  在 Windows 檔案總管中，以滑鼠右鍵按一下 [圖片專案] (的 [檔案]、[資料夾] 或 [堆疊]) ，將它們新增至佇列，或在範例應用程式中播放。 當您將範例變更為使用音樂時，請使用音樂專案。

 

 



