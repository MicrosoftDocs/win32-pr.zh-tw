---
title: PeakValue
description: PeakValue 屬性包含的16位波幅值會指定音訊內容的尖峰音量層級。
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue windows Media 格式
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "107001071"
---
# <a name="peakvalue"></a>PeakValue

**PeakValue** 屬性包含的16位波幅值會指定音訊內容的尖峰音量層級。 使用 [**AverageLevel**](averagelevel.md)時，此屬性會用於正規化。 正規化是調整音訊檔案的播放音量層級的程式，以便在相同層級和每個檔案的平均磁片區播放 loudest 部分相同。

## <a name="global-constant"></a>全域常數

g \_ wszPeakValue

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

這個屬性是由寫入器物件根據編解碼器的資訊來設定。 只有使用其中一個 Windows Media 音訊編解碼器壓縮的串流具有自動設定的值。

**PeakValue** 不是唯讀的。 但是，如果 Windows Media Player 會播放檔案，您就不應該變更此值。 Windows Media Player 使用這個來正規化播放清單中的檔案層級。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




