---
title: WM/WMADRCAverageReference
description: WM/WMADRCAverageReference 屬性包含檔案的平均磁片區層級（編碼方式）。
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/WMADRCAverageReference windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026946"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

**WM/WMADRCAverageReference** 屬性包含檔案的平均磁片區層級（編碼方式）。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。 寫入 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器的資料流程時，寫入器會根據編解碼器的資訊來設定這些值。 平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。 參考值是唯讀的。 當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




