---
title: 'WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl) '
description: 對角線轉換會沿著框架的一個角落以對角線線顯示新影像。
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471984"
---
# <a name="wmt_videoimage_transition_diagonal"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 對角線

對角線轉換會沿著框架的一個角落以對角線線顯示新影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 寬度 | <strong>fEffectPara0</strong> | 對角線區段的寬度（以圖元為單位）。 | 
| 高度 | <strong>fEffectPara1</strong> | 對角線區段的高度（以圖元為單位）。 | 
| 方向 | <strong>fEffectPara2</strong> | 決定轉換來源的邊角。設定為下列其中一項：<br /><ul><li>0-右上</li><li>1-左上</li><li>2-右下</li><li>3-左下角</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景。</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





