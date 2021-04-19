---
description: StructuredQuerySample 程式碼範例示範如何從主控台讀取行、使用系統架構加以剖析，以及顯示產生的條件樹狀結構。
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991696"
---
# <a name="structuredquerysample"></a>StructuredQuerySample

StructuredQuerySample 程式碼範例示範如何從主控台讀取行、使用系統架構加以剖析，以及顯示產生的條件樹狀結構。

本主題包含下列各節。

- [需求](#requirements)
- [下載範例](#downloading-the-sample)
- [建立範例](#building-the-sample)
- [執行範例](#running-the-sample)
- [相關主題](#related-topics)

## <a name="requirements"></a>規格需求

| 產品     | 產品版本          |
|-------------|--------------------------|
| Windows     | Windows 7、8.1 或 10    |
| Windows SDK | 7.0 或更高版本           |

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。

| Location      | 路徑 URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [StructuredQuerySample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> 針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。

## <a name="building-the-sample"></a>建立範例

1. 開啟 Windows 檔案總管，然後流覽至 **StructuredQuerySample** 專案目錄。
2. 按兩下 StructuredQuerySample .sln 檔案的圖示，在 Visual Studio 中開啟專案。

    > [!NOTE]  
    > .Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。 這不會影響範例的行為。

3. 從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1. 使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2. 在命令提示字元中，輸入 `StructuredQuerySample.exe` ，或從 Windows 檔案總管中，按兩下 StructuredQuerySample.exe 的圖示。

## <a name="related-topics"></a>相關主題

### <a name="reference"></a>參考

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**IQueryParserManager**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>其他範例

[搜尋程式碼範例](-search-samples-ovw.md)
