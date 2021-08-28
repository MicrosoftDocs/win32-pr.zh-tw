---
description: 指定描述輸入音訊內容的 WAVEFORMATEX 結構。
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: 'MFPKEY_WMAENC_ORIGWAVEFORMAT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df477daa61e39eb6b2a86aa26c27de4088e943d41f40ac9b708a0201698088c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113138"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT 屬性

指定描述輸入音訊內容的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>資料類型

VT \_ array \| vt \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 為位元組陣列) 

## <a name="remarks"></a>備註

將以 Windows Media 音訊為基礎的內容轉換成較低的位元速率時，您可以將內容的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構傳遞給編解碼器，讓編解碼器能夠優化其演算法。 這項功能稱為 smart recompression，可提供比解壓縮內容更好的結果，然後透過編解碼器將重新產生的 PCM 範例饋送回來。

傳遞 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構時，請在 **WAVEFORMATEX cbSize** 所指定之結構的結尾包含任何額外的位元組。

音訊編碼器只接受通道數目、每個樣本位數和樣本速率相同的輸入和輸出。 您只能將內容轉碼至這些參數中的較低位元速率。 在任何情況下，您都必須將內容解碼，並將未壓縮的範例作為輸入傳遞至編碼器。 設定此屬性可為編碼器提供有關已在內容上執行之處理的一些資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
