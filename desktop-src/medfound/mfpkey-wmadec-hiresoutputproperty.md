---
description: 指定音訊解碼器是否應提供高解析度的輸出。
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: 'MFPKEY_WMADEC_HIRESOUTPUT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5226babc8fd40875ec11cfa0b03345ba0b9c1a914b45b5ad79284f79d92130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872536"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>MFPKEY \_ WMADEC \_ HIRESOUTPUT 屬性

指定音訊解碼器是否應提供高解析度的輸出。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACHiResOutput

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ FALSE**

## <a name="remarks"></a>備註

將此屬性設定為 VARIANT \_ TRUE，以將多聲道或24位音訊內容或速率高於 48000 Hz 的音訊內容解碼。 如果內容是以高解析度編碼，但這個屬性是 VARIANT \_ FALSE，則適用下列行為：

-   DMO 輸出將限制為16位、48-KHz 身歷聲。
-   MFT 會列舉限制為16個位的輸出模式，而不涉及頻道計數或取樣率的變更。

高解析度音訊的屬性會在 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構中傳遞，而不是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))。

只有當解碼器正在 Windows XP 或更新版本上執行時，才能使用高解析度輸出。 無論您的應用程式執行所在的作業系統為何，都可以設定此屬性。 在 Windows XP 之前的 Windows 版本上，此解碼器將會忽略此設定並傳遞標準輸出。

許多玩家 (包括 Windows Media Player 9 系列和更新版本，) 為所有內容設定這個值。

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

 

 
