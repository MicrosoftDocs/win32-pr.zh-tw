---
title: 'WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl) '
description: 淡化至色彩的轉換是從影像溶解到純色的框架。
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000777"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>WMT \_ VIDEOIMAGE \_ 轉換 \_ 淡化 \_ 成 \_ 色彩

淡化至色彩的轉換是從影像溶解到純色的框架。

## <a name="parameters"></a>參數

下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。



| 參數         | 結構成員 | Description                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 紅色               | **fEffectPara0** | 背景色彩的紅色值。 設定為介於0和255之間的數位。                                                                                                                                                     |
| 綠色             | **fEffectPara1** | 背景色彩的綠色值。 設定為介於0和255之間的數位。                                                                                                                                                   |
| 藍色              | **fEffectPara2** | 背景色彩的藍色值。 設定為介於0和255之間的數位。                                                                                                                                                    |
| 背景權數 | **fEffectPara3** | 背景色彩的加權。 此參數會將混合中的背景色彩百分比表示為小數。 例如，若要將背景色彩 blend 為30%，請將影像70% 的混合設定為0.30。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmsdkidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片影像轉換**](video-image-transitions.md)
</dt> </dl>

 

 





