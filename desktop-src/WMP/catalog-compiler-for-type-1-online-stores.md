---
title: 類型1線上商店的目錄編譯器
description: 類型1線上商店的目錄編譯器
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player 線上商店，目錄編譯器
- 線上商店，目錄編譯器
- 輸入1個線上商店、目錄編譯器
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- 目錄編譯器
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864208"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>類型1線上商店的目錄編譯器

目錄編譯器 (catcomp.exe) 是一種命令列工具，可供型別1線上商店用來將包含線上商店目錄資料的一組 tab 鍵分隔值 (TSV) 檔案，編譯成可透過 Windows Media Player 下載的壓縮類別目錄。 目錄編譯器也會編譯目錄更新檔案，其中只包含上次目錄更新之後變更的目錄資訊。

您應在[IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)的線上商店外掛程式的執行中，提供已壓縮的類別目錄檔案或目錄更新檔案，以供下載 Windows Media Player。

一般工作

-   [從 TSV 檔案編譯完整目錄](compiling-a-full-catalog-from-tsv-files.md)
-   [從完整目錄編譯目錄更新](compiling-a-catalog-update-from-full-catalogs.md)

診斷工作

-   [顯示說明](displaying-help.md)
-   [正在抓取目錄資訊](retrieving-catalog-information.md)
-   [將更新套用至目錄](applying-an-update-to-a-catalog.md)

 

 




