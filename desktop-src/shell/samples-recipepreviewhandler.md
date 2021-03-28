---
description: 示範如何撰寫用來在 Windows 檔案總管預覽窗格或其他預覽處理常式主機內顯示檔案預覽的處理常式。
title: 配方預覽處理常式範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973496"
---
# <a name="recipe-preview-handler-sample"></a>配方預覽處理常式範例

示範如何撰寫用來在 Windows 檔案總管預覽窗格或其他預覽處理常式主機內顯示檔案預覽的處理常式。

本主題包含下列幾節：

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [取消註冊範例預覽處理常式 DLL](#unregistering-the-sample-preview-handler-dll)
-   [相關主題](#related-topics)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [RecipePreviewHandler 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **RecipePreviewHandler** 專案目錄。 例如： `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler` 。
2.  輸入 `msbuild PreviewHandlerSDKSample.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **RecipePreviewHandler** 專案目錄。
2.  按兩下 PreviewHandlerSDKSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

> [!Note]  
> 如果目標系統是64位 (x64) ，此範例預覽處理常式必須建立為64位應用程式。

 

## <a name="running-the-sample"></a>執行範例

1.  開啟 [命令提示字元] 視窗，並流覽至內建的 **RecipePreviewHandler** 專案目錄。 例如： `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler` 。 輸入 `regsvr32.exe PreviewHandlerSDKSample.dll` 以註冊處理常式。
2.  開啟 Windows 檔案總管，並顯示 [預覽] 窗格（如果尚未顯示）。
    -   **Windows 7**：按一下 [預覽] 窗格按鈕。
    -   **Windows Vista**：按一下 [ **組織** ] 功能表，移至 [ **版面** 配置] 子功能表，然後選取 [ **預覽窗格]**。
3.  使用 Windows 檔案總管流覽至 **RecipePreviewHandler** 專案目錄。
4.  選取範例檔案。

若要讓32位 (x86) 和64位 (x64) 輸出可在64位版本的 Windows 上運作，請將 **AppId** 值設定為 WOW64 代理主機 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` ，如下列程式碼所示。


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a>取消註冊範例預覽處理常式 DLL

-   開啟 [命令提示字元] 視窗，然後輸入 `regsvr32.exe /u PreviewHandlerSDKSample.dll` 以取消註冊處理常式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> </dl>

 

 
