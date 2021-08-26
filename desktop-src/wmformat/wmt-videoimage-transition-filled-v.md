---
title: 'WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl) '
description: 已填滿的 V 轉換會顯示來自框架某一端的三角形中的新影像。
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466155"
---
# <a name="wmt_videoimage_transition_filled_v"></a>WMT \_ VIDEOIMAGE \_ 轉換已 \_ 填滿 \_ V

已填滿的 V 轉換會顯示來自框架某一端的三角形中的新影像。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 寬度 | <strong>fEffectPara0</strong> | 填滿 V 的寬度（以圖元為單位）。 | 
| 高度 | <strong>fEffectPara1</strong> | 填滿 V 的高度（以圖元為單位）。 | 
| 方向 | <strong>fEffectPara2</strong> | 填滿 V 來源的方向。設定為下列其中一個值：<br /><ul><li>0-從框架左邊進入。</li><li>1-從框架的右邊進入。</li><li>2-從框架底部進入。</li><li>3-從框架頂端進入。</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





