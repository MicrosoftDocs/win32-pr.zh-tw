---
title: 'WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl) '
description: 矩形轉換會顯示框架內矩形內的新影像。
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8721455c09a263d9c856358d2ca55bb818ac48e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467395"
---
# <a name="wmt_videoimage_transition_rectangle"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 矩形

矩形轉換會顯示框架內矩形內的新影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 中心 X | <strong>fEffectPara0</strong> | 矩形中央的相對於影片框架的 X 座標。 | 
| 中心 Y | <strong>fEffectPara1</strong> | 矩形中央的 Y 座標（相對於影片框架）。 | 
| 寬度 | <strong>fEffectPara2</strong> | 矩形的寬度（以圖元為單位）。 | 
| 高度 | <strong>fEffectPara3</strong> | 矩形的高度（以圖元為單位）。 | 
| Composition | <strong>fEffectPara4</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





