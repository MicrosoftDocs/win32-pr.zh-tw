---
description: 媒體類型
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: '媒體類型 (媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321624"
---
# <a name="media-types-media-foundation"></a>媒體類型 (媒體基礎) 

*媒體類型* 是描述媒體資料流程格式的方式。 在媒體基礎中，媒體類型會以 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面表示。 應用程式會使用媒體類型來探索媒體檔案或媒體資料流程的格式。 媒體基礎管線中的物件會使用媒體類型來協調其傳遞或接收的格式。

此章節包含下列主題。



| 主題                                                                    | 描述                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [關於媒體類型](about-media-types.md)                               | 媒體基礎媒體類型的一般總覽。                             |
| [媒體類型 Guid](media-type-guids.md)                                 | 列出主要類型和子類型的已定義 Guid。                            |
| [音訊媒體類型](audio-media-types.md)                               | 如何建立音訊格式的媒體類型。                                     |
| [影片媒體類型](video-media-types.md)                               | 如何建立影片格式的媒體類型。                                     |
| [完成和部分媒體類型](complete-and-partial-media-types.md) | 描述完整媒體類型與部分媒體類型之間的差異。   |
| [媒體類型轉換](media-type-conversions.md)                     | 如何在媒體基礎媒體類型與較舊的格式結構之間轉換。 |
| [媒體類型 Helper 函式](media-type-helper-functions.md)           | 可操作或從媒體類型取得資訊的函式清單。        |
| [媒體類型的偵錯工具代碼](media-type-debugging-code.md)               | 示範如何在偵錯工具中查看媒體類型的範例程式碼。                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎基本](media-foundation-primitives.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 



