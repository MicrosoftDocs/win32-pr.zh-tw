---
title: 'WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl) '
description: 頁面變換轉換會以頁面翻轉效果轉換舊影像，並在下方顯示新的影像。
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474974"
---
# <a name="wmt_videoimage_transition_page_roll"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 頁面 \_ 滾動

頁面變換轉換會以頁面翻轉效果轉換舊影像，並在下方顯示新的影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 半徑 | <strong>fEffectPara0</strong> | 頁面滾動效果中的滾動半徑。 | 
| 距離 | <strong>fEffectPara1</strong> | 頁面滾動效果所顯示的新影像數量（以圖元為單位）。 | 
| 方向 | <strong>fEffectPara2</strong> | 頁面變換來源的影片框架邊角或側邊。設定為下列其中一個值：<br /><ul><li>0-左邊</li><li>1-右端</li><li>2-下</li><li>3-上方</li><li>4-左下角</li><li>5-右下角</li><li>6-左上角</li><li>7-右上角</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





