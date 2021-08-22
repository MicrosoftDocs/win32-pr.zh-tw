---
title: AverageLevel
description: AverageLevel 屬性包含16位的值，用來指定音訊內容的平均音量層級。
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel windows Media 格式
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028156"
---
# <a name="averagelevel"></a>AverageLevel

**AverageLevel** 屬性包含16位的值，用來指定音訊內容的平均音量層級。 使用 [**PeakValue**](peakvalue.md)時，此屬性會用於正規化。 正規化是調整音訊檔案的播放音量層級的程式，以便在相同層級和每個檔案的平均磁片區播放 loudest 部分相同。

## <a name="global-constant"></a>全域常數

g \_ wszAverageLevel

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

這個屬性是由寫入器物件根據編解碼器的資訊來設定。 只有使用其中一個 Windows Media 音訊編解碼器壓縮的串流具有自動設定的值。

**AverageLevel** 不是唯讀的。 但是，如果 Windows Media Player 會播放檔案，您就不應該變更此值。 Windows Media Player 使用這個來正規化播放清單中的檔案層級。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




