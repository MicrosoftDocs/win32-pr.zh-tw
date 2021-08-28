---
title: 'WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl) '
description: 鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。 此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472964"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 鳶尾花

鳶尾花轉換會沿著 X 軸和 y 軸顯示新的影像。 此轉換的視覺效果是新的影像會出現在擴展交叉到達框架的所有側邊。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 中心 X | <strong>fEffectPara0</strong> | 相對於影片框架的 X 座標，鳶尾花效果的中心。 | 
| 中心 Y | <strong>fEffectPara1</strong> | 相對於影片框架的 Y 座標，鳶尾花效果的中心。 | 
| 寬度 | <strong>fEffectPara2</strong> | 垂直線的寬度，以圖元為單位顯示新影像。 | 
| 高度 | <strong>fEffectPara3</strong> | 水平線的高度會顯示新影像（以圖元為單位）。 | 
| Composition | <strong>fEffectPara4</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





