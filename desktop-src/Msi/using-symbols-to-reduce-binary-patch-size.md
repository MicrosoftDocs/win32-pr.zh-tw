---
description: 針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: 使用符號來減少二進位修補程式大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c11a1a6b058db8c9f4a7c9bde897034c3b4affa8c02d1b049d754013f4455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804080"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>使用符號來減少二進位修補程式大小

針對您的目標和升級映射二進位檔使用公用符號，可減少大約一半的二進位修補程式大小。 實際的縮減取決於所使用的符號。 請注意，使用符號可能會導致修補程式建立速度變慢，因為處理符號檔需要較長的時間。

若要使用符號來縮減二進位修補程式的大小，您必須為目標和升級映射二進位檔提供符號。 在 [TargetImages](targetimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行和 [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行中指定符號。 您必須使用 Visual C++ 在程式資料庫 (PDB) 檔案格式產生符號。 較新版本的 Visual C++ 會提供 PDB 檔案中的所有必要資訊。 較舊版本的 Visual C++ 也會產生 debug (DBG) 檔案格式。 在此情況下，SymbolsPaths 值應該指定 PDB 和 DBG 檔案的位置。

例如，修補程式的 TargetImage 可能是隨附于 Windows 2000 的安裝套件，而且會安裝 MSI.DLL 的1.1.1029.0 版本。 UpgradedImage 可能是隨附于 Windows 2000 Service Pack 1 (SP1) 的更新版安裝套件，而且會安裝 MSI.DLL 的1.11.1314.0 版本。 您必須建立兩個 Patch 建立屬性 (PCP) 檔案，其中一個檔案的 [TargetImages](targetimages-table-patchwiz-dll-.md) 和 [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) 資料表的 SymbolPaths 資料行都是 Null (空白) ，另一個則是 SymbolPaths 和 TargetImages 資料表的 UpgradedImages 資料行，並以二進位檔的符號位置填入。 在此情況下，不使用符號所產生的修補程式大小，大約是使用符號產生之修補程式大小的三倍。

Mpatch.exe 公用程式可以用來測試單一檔案的二進位修補程式產生，以及檢查符號是否有效。 Mpatch.exe 公用程式包含在[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。 Mpatch.exe 的輸出會指出符號是否不相符。

例如，輸入下列命令列來檢查符號是否有效。

**mpatch.exe-NEWSYMPATH： d： \\ update-OLDSYMPATH： d： \\ target d： \\ target \\example.dll d： \\ update \\example.dll 範例 .pat**

如果符號不在正確的位置，Mpatch.exe 的輸出可能會包含下列警告。

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



