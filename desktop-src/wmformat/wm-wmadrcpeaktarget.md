---
title: WM/WMADRCPeakTarget
description: WM/WMADRCPeakTarget 屬性包含使用者要求的最大磁片區層級。 動態範圍控制的 Windows Media Player 會使用這個值。
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/WMADRCPeakTarget windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590678"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

**WM/WMADRCPeakTarget** 屬性包含使用者要求的最大磁片區層級。 動態範圍控制的 Windows Media Player 會使用這個值。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。 寫入 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器的資料流程時，寫入器會根據編解碼器的資訊來設定這些值。 平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。 參考值是唯讀的。 當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




