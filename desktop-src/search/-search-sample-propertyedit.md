---
description: PropertyEdit 程式碼範例示範如何將標準屬性名稱轉換成 PROPERTYKEY、將屬性存放區的值設定為專案的值，然後將資料寫回檔案資料流程。
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944419f990c8f1f8b52706dbab0b08102829e77a5bfa8a91c72a5bc16eddfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944667"
---
# <a name="propertyedit"></a>PropertyEdit

PropertyEdit 程式碼範例示範如何將標準屬性名稱轉換成 PROPERTYKEY、將屬性存放區的值設定為專案的值，然後將資料寫回檔案資料流程。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="requirements"></a>規格需求



| 產品     | 最小產品版本 |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| 位置      | 路徑 URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [PropertyEdit 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> 針對所有版本的 Windows （包括 Windows 7），建議您直接從 GitHub 下載這些範例，以取得最新版本。

 

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **PropertyEdit** 專案目錄。 
2.  輸入 `msbuild PropertyEdit.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **PropertyEdit** 專案目錄。
2.  按兩下 PropertyEdit .sln 檔案的圖示，在 Visual Studio 中開啟專案。
    > [!Note]  
    > .Sln 副檔名不會顯示在 [預設資料夾設定] 下。 在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。

     

3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令提示字元中，輸入 `PropertyEdit.exe` ，或從 Windows 檔案總管中，按兩下 PropertyEdit.exe 的圖示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[搜尋程式碼範例](-search-samples-ovw.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[關於屬性和屬性處理常式](../properties/building-property-handlers-properties.md)
</dt> <dt>

[屬性描述架構](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
