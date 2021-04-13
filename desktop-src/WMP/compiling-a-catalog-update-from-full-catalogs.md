---
title: 從完整目錄編譯目錄更新
description: 從完整目錄編譯目錄更新
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player 線上商店，編譯目錄
- 線上商店，編譯目錄
- 輸入1個線上商店，編譯目錄
- Windows Media Player 線上商店、類別目錄更新
- 線上商店、類別目錄更新
- 輸入1個線上商店、類別目錄更新
- Windows Media Player 線上商店、完整目錄
- 線上商店、完整目錄
- 輸入1個線上商店、完整目錄
- 編譯目錄
- 目錄更新
- 完整目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314214"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>從完整目錄編譯目錄更新

您可以使用下列語法來建立包含已編譯之類別目錄的兩個版本之間變更的目錄更新，其中 *path1* 是包含第一個目錄的目錄， *path2* 是包含第二個目錄的目錄，而且可以選擇性地包含 debug，以在畫面上顯示詳細的錯誤資訊。 類別目錄檔案必須是未壓縮的格式—已編譯之目錄的檔案名會是 wmdb，而不是 wmdb. lz。


```C++
catcomp diff <path1> <path2> [debug]
```



例如，如果 C： \\ Catalog210 \\ 目錄包含完整編譯目錄的210版，而 c： \\ Catalog211 \\ 包含211版，則下列命令會建立一個差異檔案，其中包含兩個版本之間的變更：


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



若要顯示詳細的錯誤資訊，您可以新增選擇性的 debug 參數，如下所示：


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



如果編譯成功，catcomp.exe 會建立如下所列的輸出檔案，並將它們儲存在包含第一個目錄的目錄中。



| 檔案名稱             | 描述                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 目錄。差異          | 未壓縮的已編譯差異檔案。                                                                                                                                                           |
| catalog. lz       | 目錄更新檔案的壓縮版本。 您的外掛程式可將此檔案的位置提供給 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)中的 Windows Media Player。 |
| catalog. wmdb delta    | 中繼輸出檔。 Windows Media Player 未使用                                                                                                                                       |
| catalog. wmdb. 修改 | 中繼輸出檔。 Windows Media Player 未使用                                                                                                                                       |



 

 

 




