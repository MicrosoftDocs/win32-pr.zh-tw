---
title: 像素格式函數
description: 下列 Windows 函數會管理像素格式。
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- WGL 函式，像素格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c4b82a2b6cd91dd007cecf78065fa0c01204ecf468017ec7e121bd764c9ff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486328"
---
# <a name="pixel-format-functions"></a>像素格式函數

下列 Windows 函數會管理像素格式。



| Windows功能                                               | Description                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | 取得裝置內容的像素格式，此格式最符合指定的像素格式。                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | 將裝置內容的目前像素格式設定為像素格式索引所指定的像素格式。                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | 取得裝置內容目前像素格式的像素格式索引。                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | 針對裝置內容和像素格式索引，以像素格式的屬性填入 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構。 |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | 抓取增強型中繼檔的像素格式資訊。                                                                                                          |



 

[**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)函式會傳回以一為基礎的像素格式索引，以識別最符合裝置內容支援的像素格式。

[**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)函式會使用以一為基礎的像素格式索引來識別所要的格式。 一般來說，您會呼叫 **ChoosePixelFormat** 來尋找最符合的像素格式，然後使用 **ChoosePixelFormat** 的結果來呼叫 **SetPixelFormat** 。

如果您針對參考視窗的裝置內容呼叫 **SetPixelFormat** ， **SetPixelFormat** 也會變更視窗的像素格式。 設定視窗的像素格式可能會導致視窗管理員和多執行緒應用程式的大複雜，因此不允許這種情況。 您只能將視窗的像素格式設定為一次;之後，就無法變更視窗的像素格式。

[**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)函式會傳回以一為基礎的像素格式索引。

[**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)函式會以下列參數作為參數：

-   裝置內容的控制碼
-   像素格式索引
-   [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)資料結構的指標

[**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)函式會以適當設定的 **PIXELFORMATDESCRIPTOR** 成員傳回。

**GetEnhMetaFilePixelFormat** 函式會傳回中繼檔的像素格式大小，並抓取中繼檔的像素格式資訊。

 

 




