---
title: 'WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl) '
description: 翻轉轉換會透過框架的中央旋轉 y 軸上的舊影像。 新映射會顯示為舊影像的背面。
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a3bfe94e001c6a65256facd5484a015d00f245
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475754"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 翻轉

翻轉轉換會透過框架的中央旋轉 y 軸上的舊影像。 新映射會顯示為舊影像的背面。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。




| 參數 | 結構成員 | Description | 
|-----------|------------------|-------------|
| 角度 | <strong>fEffectPara0</strong> | 旋轉的角度，從0.0 到180.0 度。 | 
| Composition | <strong>fEffectPara1</strong> | 設定為下列其中一個值：<ul><li>0-指定一般組合，其中上一個影像是背景，而目前影像是前景。</li><li>1-指定反轉組合，其中目前影像是背景影像，而上一個影像是前景</li></ul> | 




 

## <a name="remarks"></a>備註

您可以將這項轉換的效果視覺化，就像這兩個影像都是將兩個影像都與後置中的實體相片一起進行。 轉換的效果與將兩個這類相片放在下邊緣，並將它們旋轉180度的效果相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





