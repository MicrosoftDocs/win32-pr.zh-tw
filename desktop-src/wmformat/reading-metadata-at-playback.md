---
title: 在播放時讀取中繼資料
description: 在播放時讀取中繼資料
ms.assetid: 48d37a9e-5e22-4298-abc4-b69998906dcb
keywords:
- Windows媒體格式 SDK，讀取中繼資料
- Windows媒體格式 SDK，非同步讀取器
- Windows媒體格式 SDK，同步讀取器
- Advanced Systems Format (ASF) ，讀取中繼資料
- ASF (Advanced Systems Format) ，讀取中繼資料
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 非同步讀取器，讀取中繼資料
- 同步讀取器，讀取中繼資料
- 中繼資料，在播放時讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f62100da8c2f27e626e27ae6686e08f7217867ec2775f69292aac495d218fcb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027346"
---
# <a name="reading-metadata-at-playback"></a>在播放時讀取中繼資料

非同步讀取器物件和同步讀取器物件都可以從已載入之 ASF 檔案的標頭讀取中繼資料。 讀取檔案時，中繼資料屬性都是唯讀的。 這兩個讀取器物件都可以針對 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 和 [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) 介面進行查詢。

如需存取中繼資料的詳細資訊，請參閱 [使用中繼資料](working-with-metadata.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 




