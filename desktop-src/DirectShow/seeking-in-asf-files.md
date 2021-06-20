---
description: 瞭解 WM ASF 讀取器如何針對在 DirectShow 中具有時態性索引的 Windows Media 內容，執行非常精確的時態搜尋。
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: '在 ASF 檔案中搜尋 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405581"
---
# <a name="seeking-in-asf-files-directshow"></a>在 ASF 檔案中搜尋 (DirectShow) 

透過其 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面的 [WM ASF 讀取器](wm-asf-reader-filter.md)，可以在具有時態性索引的 Windows Media 內容上執行非常精確的時態搜尋。  (所有框架索引的內容也包含時態性索引 ) 。在 WM ASF 讀取器中，不直接支援以框架精確的搜尋，但如果您需要這項功能，有方法可以這麼做。 首先，使用 Windows Media Format SDK 來建立同步讀取器物件的實例、開啟檔案、取得與指定框架相關聯的時間戳記，然後使用 DirectShow **IMediaSeeking** 介面來搜尋該時間。 [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)介面不支援以畫面格精確的形式搜尋 Windows Media 內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



