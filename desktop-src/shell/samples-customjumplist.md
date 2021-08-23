---
description: 示範如何建立應用程式的自訂捷徑清單，包括新增自訂分類和工作。
title: 自訂跳躍清單範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968827"
---
# <a name="custom-jump-list-sample"></a>自訂跳躍清單範例

示範如何建立應用程式的自訂捷徑清單，包括新增自訂分類和工作。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| 位置      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [CustomJumpList 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **CustomJumpList** 專案目錄。
2.  輸入 `msbuild CustomJumpListSample.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **CustomJumpList** 專案目錄。
2.  按兩下 CustomJumpListSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `CustomJumpListSample.exe` 。 或者，從 Windows 檔案總管按兩下 CustomJumpListSample.exe 的圖示。
3.  在第一次執行此範例時，必須以系統管理員的身分執行，讓它可以安裝必要的檔案類型註冊。 在註冊檔案類型之後，範例可以作為標準使用者來執行。
4.  從範例應用程式的功能表中選取 [選項]，以查看它們如何影響工作列中的應用程式捷徑清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> </dl>

 

 



