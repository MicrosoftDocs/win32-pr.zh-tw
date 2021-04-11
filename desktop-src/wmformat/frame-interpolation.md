---
title: 框架插補
description: 框架插補
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK，框架插補
- 編解碼器，框架插補
- 框架插補
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023044"
---
# <a name="frame-interpolation"></a>框架插補

框架插補是以兩個連續的編碼影片框架中的資料為基礎建立中繼影片框架的程式。 實際上，框架插補會在解碼時，增加編碼影片的 [*畫面播放速率*](wmformat-glossary.md) 。 您可以使用畫面格插補來改善以較低畫面播放速率播放影片的平滑。

因為這是解碼功能，所以它不會牽涉到任何特殊的編碼選項，也不會增加內容的額外負荷。 框架插補會指定為讀取器物件中的輸出設定。

只有 Windows Media 視訊9編解碼器支援框架插補。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**編解碼器功能**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**輸出設定**](output-settings.md)
</dt> </dl>

 

 




