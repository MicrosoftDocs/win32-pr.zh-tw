---
description: 推送來源篩選範例
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: 推送來源篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747788"
---
# <a name="push-source-filters-sample"></a>推送來源篩選範例

## <a name="description"></a>描述

此範例包含一組三個來源篩選器，可提供下列來源資料作為影片串流：

-   CPushSourceBitmap：從目前目錄載入的單一點陣圖 () 
-   CPushSourceBitmapSet：從目前目錄載入 (點陣圖集合) 
-   CPushSourceDesktop：目前桌面映射的複本 (僅限 GDI) 

## <a name="usage"></a>使用方式

若要使用篩選，請將它載入至 GraphEdit 並轉譯其輸出圖釘。 這會連接影片轉譯器 (可能會有色彩空間轉換器篩選) 並可讓您顯示輸出。 如果您想要將輸出轉譯成 AVI 檔案，請載入 AVI Mux、載入檔案寫入器篩選器、提供輸出名稱給檔案寫入器，然後轉譯 PushSource 濾波器的輸出圖釘。 您也可以載入和連接影片壓縮機、影片效果等等。

> [!Note]  
> Desktop capture 篩選不支援硬體重迭，因此它不會將轉譯的影片捕獲到重迭表面或透過硬體重迭顯示的資料指標。 它會使用 GDI 將目前的桌面影像轉換為點陣圖，並以媒體範例形式傳遞至輸出圖釘。

 

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ PushSource。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 



