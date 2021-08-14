---
description: 檔案庫取代檔資料夾
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: 檔案庫取代檔資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329668"
---
# <a name="file-library-replaces-document-folder"></a>檔案庫取代檔資料夾

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器**-Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -高  











## <a name="description"></a>Description

程式庫提供集中的類似資料夾體驗，可跨多個位置（本機和遠端）進行檔案儲存、搜尋和存取。

一般檔案對話方塊所使用的預設位置 (例如，[開啟] 和 [儲存) ] 已從 [檔] 資料夾變更為 [文件庫]。 消費者介面不會變更，但使用者現在可以使用各種排列檢視來查看、流覽和搜尋程式庫。 檔案將會儲存到程式庫預設儲存位置，除非使用者變更預設儲存位置或選擇不同的資料夾。

開發人員可以建立自己的程式庫，或使用 IShellLibrary 介面將位置新增至現有的程式庫。 使用者可以使用已知的資料夾系統來尋找程式庫 (例如 FOLDERID \_ DocumentsLibrary) 。

## <a name="manifestation-of-impact"></a>影響的表現

程式庫本身就是檔案，而不是資料夾。 因此，因為應用程式嘗試將檔案串連至檔案，所以路徑操作可能會導致錯誤。

## <a name="solution"></a>解決方案

使用 IFileDialog 時，您必須使用 GetResult 方法，而不是 GetFolder 和 GetFilename 的組合，如同您在先前的作業系統版本中所做的一樣。 盡可能使用 Shell Api 來與 Shell 命名空間中的專案互動和操作 (例如，IShellItem) 。

## <a name="leveraging-feature-capabilities"></a>運用功能功能

如果您想要建立自己的程式庫，或將位置新增至現有的程式庫，您必須使用 IShellLibrary API。 程式庫本身就是 Shell 資料夾，因此您可以像任何其他 Shell 資料夾一樣來列舉它們。

## <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

使用 [一般檔案] 對話方塊可確保使用者可以直接儲存在其程式庫中。

## <a name="links-to-other-resources"></a>其他資源的連結

-   **Windows 程式庫：**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **與程式庫保持同步：**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



