---
title: WM/WMADRCPeakReference
description: WM/WMADRCPeakReference 屬性包含檔案的最大磁片區層級（編碼方式）。 動態範圍控制的 Windows Media Player 會使用這個值。 此值是由編解碼器設定的，而且是唯讀的。
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- WM/WMADRCPeakReference windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e5abf41b52b615030c07b532fc3d75e40bd898a409e0f5ecd2b15541c8c0df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027530"
---
# <a name="wmwmadrcpeakreference"></a>WM/WMADRCPeakReference

**WM/WMADRCPeakReference** 屬性包含檔案的最大磁片區層級（編碼方式）。 動態範圍控制的 Windows Media Player 會使用這個值。 此值是由編解碼器設定的，而且是唯讀的。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMADRCPeakReference

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

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




