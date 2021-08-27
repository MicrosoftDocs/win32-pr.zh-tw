---
description: 示範如何將專案加入至應用程式的自動捷徑清單，包括在常見和最近類別的顯示之間切換。
title: 自動跳躍清單範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4dcb2146c8db8eda0280b3ff7a34a19faf4ac172036ae7a4e61131b50fde2d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090188"
---
# <a name="automatic-jump-list-sample"></a>自動跳躍清單範例

示範如何將專案加入至應用程式的自動捷徑清單，包括在常見和最近類別的顯示之間切換。

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

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [AutomaticJumpList 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **AutomaticJumpList** 專案目錄。
2.  輸入 `msbuild AutomaticJumpListSample.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **AutomaticJumpList** 專案目錄。
2.  按兩下 AutomaticJumpListSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `AutomaticJumpListSample.exe` 。 或者，從 Windows 檔案總管按兩下 AutomaticJumpListSample.exe 的圖示。
3.  在第一次執行此範例時，必須以系統管理員的身分執行，讓它可以安裝必要的檔案類型註冊。 在註冊檔案類型之後，範例可以作為標準使用者來執行。
4.  從範例應用程式的功能表中選取選項，包括透過 [ **開啟** ] 對話方塊選取 .txt 或 .doc 檔，以查看它們如何影響工作列中的應用程式捷徑清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> </dl>

 

 



