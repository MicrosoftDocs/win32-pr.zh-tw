---
description: 示範如何透過 System.AppUserModel.ID 屬性控制應用程式視窗的工作列群組行為。
title: 應用程式使用者模型識別碼視窗屬性範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973544"
---
# <a name="application-user-model-id-appid-window-property-sample"></a>應用程式使用者模型識別碼 (AppID) 視窗屬性範例

示範如何透過 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性控制應用程式視窗的工作列群組行為。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例會示範如何使用透過 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)取得的視窗 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)實作為來設定 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)屬性。

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [AppUserModelIDWindowProperty 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **AppUserModelIDWindowProperty** 專案目錄。
2.  輸入 `msbuild AppUserModelIDWindowProperty.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **AppUserModelIDWindowProperty** 專案目錄。
2.  按兩下 AppUserModelIDWindowProperty .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中，輸入 `AppUserModelIDWindowProperty.exe` 。 或者，從 Windows 檔案總管按兩下 AppUserModelIDWindowProperty.exe 的圖示。
3.  若要示範應用程式使用者模型識別碼的效果 (AppUserModelIDs) 在工作列群組上，請同時啟動至少三個應用程式實例。
4.  使用功能表在三個視窗中設定不同的 AppUserModelID。 請注意，每個不同的 AppUserModelID 都會產生個別的工作列按鈕，而且 windows 可以在執行時間變更其身分識別。
5.  將至少兩個視窗設定為第二個 AppUserModelID。 請注意，它們都會移至相同的工作列群組。
6.  在工作列上按一下滑鼠右鍵，**然後在內容功能表中選取**[內容]，以開啟 [**工作列] 和 [開始] 功能表 [屬性**] 視窗。 變更 **工作列按鈕：** [ **當工作列已滿時組合** ] 與 [ **永遠不合並** 值] 之間的下拉式清單。 請注意，每個視窗都可以取得個別的按鈕，但按鈕會依 AppUserModelID 分組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> </dl>

 

 
