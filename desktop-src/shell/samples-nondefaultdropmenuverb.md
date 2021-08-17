---
description: 示範如何延伸拖放快捷方式功能表 (有時也稱為內容功能表) 。
title: NonDefaultDropMenuVerb 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1c4623b9143e0a23762cfc44dd8dfc4f46b827a0f6433098d45d8a784ead81f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968787"
---
# <a name="nondefaultdropmenuverb-sample"></a>NonDefaultDropMenuVerb 範例

示範如何延伸拖放快捷方式功能表 (有時也稱為內容功能表) 。

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
| GitHub  | [NonDefaultDropMenuVerb 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **NonDefaultDropMenuVerb** 專案目錄。
2.  輸入 `msbuild NonDefaultDropMenuVerb.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **NonDefaultDropMenuVerb** 專案目錄。
2.  按兩下 NonDefaultDropMenuVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新 DLL 檔案的目錄。
2.  將 NonDefaultDropMenuVerb.dll 複製到系統目錄 (例如，C： \\ Windows \\ System32) 。
3.  在命令提示字元中，輸入 `regedit NonDefaultDropMenuVerb.reg` 。
4.  使用滑鼠右鍵將檔案從一個資料夾拖曳到另一個資料夾。 您將會看到放置作業的其他功能表項目。

 

 



