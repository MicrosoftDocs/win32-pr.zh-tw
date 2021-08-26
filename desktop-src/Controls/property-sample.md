---
title: 屬性範例
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 深入瞭解：屬性範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f17e12031b326566e6b948b05dae5851ec4aabd1cc7fd0a0281fc9d1a89c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061638"
---
# <a name="property-sample"></a>屬性範例

本主題說明屬性範例程式碼範例。 它包含下列區段：

-   [說明](#description)
-   [最低需求](#minimum-requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>描述

屬性範例會示範如何執行三種不同的屬性工作表樣式：強制回應、非模式和 wizard。 它也會示範如何使用 [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) 函式來修改建立之前或之後的屬性工作表對話方塊。

## <a name="minimum-requirements"></a>最低需求



| 產品          | 版本                              |
|------------------|--------------------------------------|
| DLL              | comctl32.dll 版本4。0             |
| 作業系統 | Windows 95、Microsoft Windows NT 3。1 |



 

## <a name="downloading-the-sample"></a>下載範例

屬性範例會安裝為[Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)的一部分，並可在下列位置中取得。



| 位置    | 路徑/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | % Program Files% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ 控制項 \\ 通用 \\ 屬性 |



 

## <a name="building-the-sample"></a>建立範例

若要使用命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至專案目錄。
2.  輸入 `msbuild [project file]`。

若要使用 Visual Studio 建立範例：

1.  開啟 Windows 檔案總管並流覽至專案目錄。
2.  按兩下 vcproj 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表中，選取 [ **建立方案** ] 來建立方案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性工作表](property-sheets.md)
</dt> </dl>

 

 




