---
title: '在 ASF 檔案中搜尋 (Windows Media Format 11 SDK) '
description: 瞭解 WM ASF 讀取器如何針對在 Windows media Format 11 SDK 中具有時態性索引的 Windows Media 內容，執行非常精確的時態搜尋。
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK，在 ASF 檔案中搜尋
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，搜尋
- ASF (Advanced Systems Format) ，搜尋
- DirectShow，在 ASF 檔案中搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409881"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>在 ASF 檔案中搜尋 (Windows Media Format 11 SDK) 

透過其 **IMediaSeeking** 介面的 [WM ASF 讀取器](wm-asf-reader-filter.md)，可以在具有時態性索引的 Windows Media 內容上執行非常精確的時態搜尋。  (所有框架索引的內容也包含時態性索引 ) 。在 WM ASF 讀取器中，不直接支援以框架精確的搜尋，但如果您需要這項功能，有方法可以這麼做。 首先，使用 Windows Media Format SDK 來建立同步讀取器物件的實例、開啟檔案、取得與指定框架相關聯的時間戳記，然後使用 DirectShow **IMediaSeeking** 介面來搜尋該時間。 DirectShow **IVideoFrameStep** 介面不支援以畫面格精確的形式搜尋以 Windows Media 為基礎的內容。 Windows Media 格式 SDK 中的 DSSeekFm 範例會示範如何使用 WM ASF 讀取器執行框架精確的搜尋。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WM ASF 讀取器篩選器**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




