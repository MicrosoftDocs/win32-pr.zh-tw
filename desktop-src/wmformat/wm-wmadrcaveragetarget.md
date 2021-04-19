---
title: WM/WMADRCAverageTarget
description: WM/WMADRCAverageTarget 屬性包含使用者要求的平均磁片區層級。 動態範圍控制的 Windows Media Player 會使用這個值。
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- WM/WMADRCAverageTarget windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967869"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

**WM/WMADRCAverageTarget** 屬性包含使用者要求的平均磁片區層級。 動態範圍控制的 Windows Media Player 會使用這個值。

## <a name="global-constant"></a>全域常數

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

有四個屬性用於動態範圍控制的 Windows Media Player： **wm/WMADRCAverageReference**、 **wm/WMADRCPeakReference**、 **wm/WMADRCAverageTarget** 和 **WM/WMADRCPeakTarget**。 使用 Windows Media 音訊9編解碼器或 Windows Media 音訊 9 Professional 編解碼器撰寫串流時，寫入器會根據編解碼器的資訊來設定這些值。 平均值會設定為數據流的平均磁片區層級，而尖峰值會設定為數據流中的最大磁片區層級。 參考值是唯讀的。 當播放檔案以記錄使用者的動態範圍控制喜好設定時，會 Windows Media Player 設定目標值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




