---
title: 設定畫面抓取資料流程
description: 設定畫面抓取資料流程
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- 串流，設定畫面抓取資料流程
- 編解碼器，設定畫面抓取資料流程
- 畫面抓取資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0814525f57a540fe491bb1dd5425e4a0ecf4dc024a31ab0d2f468c3856921a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591798"
---
# <a name="configuring-screen-capture-streams"></a>設定畫面抓取資料流程

使用 Windows 媒體® Video 9 螢幕編解碼器的串流，是由應用程式以與一般影片串流相同的方式進行設定。 但是，如果您將影片複雜性等級設定為0，則寫入器會忽略任何以 [**IWMVideoMediaProps：： SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality)設定的影片品質值。 如需詳細資訊，請參閱[使用 Windows Media 視訊9螢幕編解碼器取得良好的結果](getting-good-results-with-the-windows-media-video-9-screen-codec.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定影片串流**](configuring-video-streams.md)
</dt> </dl>

 

 




