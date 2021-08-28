---
title: 'WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl) '
description: 滾輪轉換會在一般的軸點周圍旋轉四行（例如滾輪的輪輻）來顯示新的影像。
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b77e8640f21bd06194b2fe6b1e7048d85b323e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469265"
---
# <a name="wmt_videoimage_transition_wheel"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 輪子

滾輪轉換會在一般的軸點周圍旋轉四行（例如滾輪的輪輻）來顯示新的影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 中心 X | <strong>fEffectPara0</strong> | 滾輪效果中心相對於影片框架的 X 座標。 | 
| 中心 Y | <strong>fEffectPara1</strong> | 滾輪效果中間的 Y 座標（相對於影片框架）。 | 
| 角度 | <strong>fEffectPara2</strong> | 滾輪效果輪輻的旋轉角度（以度為單位）。 值為0.0 表示舊影像，而不會顯示任何新的影像。 值為90.0 表示已完全顯示新的影像。從0.0 到90.0 的移動會顯示為輪輻的順時針旋轉。<br /> | 
| Composition | <strong>fEffectPara3</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





