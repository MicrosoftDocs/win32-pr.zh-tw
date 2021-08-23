---
description: 有兩種類型的筆刷：邏輯和實體。
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: 關於筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c94ea9dac021a013ccc4ef624f9b00a3234102ac905999cb7c085148be91b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602788"
---
# <a name="about-brushes"></a>關於筆刷

有兩種類型的筆刷：邏輯和實體。 *邏輯筆刷* 是應用程式用來繪製圖案的理想點陣圖描述。 *實體筆刷* 是設備磁碟機根據應用程式的邏輯筆刷定義所建立的實際點陣圖。 如需點陣圖的詳細資訊，請參閱 [點陣圖](bitmaps.md)。

當應用程式呼叫其中一個建立筆刷的函式時，它會抓取一個控點來識別邏輯筆刷。 當應用程式將此控制碼傳遞至 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式時，對應的顯示或印表機的設備磁碟機會建立實體筆刷。

下列主題描述筆刷：

-   [筆刷來源](brush-origin.md)
-   [邏輯筆刷類型](logical-brush-types.md)
-   [模式區塊傳輸](pattern-block-transfer.md)
-   [啟用 ICM 的筆刷函數](icm-enabled-brush-functions.md)

 

 



