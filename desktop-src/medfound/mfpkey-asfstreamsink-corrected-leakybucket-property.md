---
description: 指定 &\# 0034; 有漏洞 bucket&\# 0034; ASF 媒體接收器上的資料流程參數。
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: 'MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb41de92f160e3d73c7d15721dae3015efc0ad1bc1a982d1a22c542d311b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874075"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>MFPKEY \_ ASFSTREAMSINK 已 \_ 更正的 \_ LEAKYBUCKET 屬性

指定 "有漏洞 bucket" 參數 (查看 ASF 媒體接收器上資料流程的備註) 。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** 值的陣列 (**CAUL**) 

VT \_ 向量 \| vt \_ UI4

**科爾**



## <a name="remarks"></a>備註

應用程式可以在資料流程的媒體類型經過協商之後，于 ASF 媒體接收器的資料流程上設定此屬性。 您可以使用這個屬性來指定 Windows 媒體編解碼器將使用的實際緩衝區視窗。 您可以使用 **IWMCodecLeakyBucket** 介面（記載于 Windows 媒體格式 SDK）取得編解碼器的資訊。

這個屬性的值是下列順序的三個 **DWORD** 值的陣列：

-   位元速率，以每秒位數為單位。
-   緩衝區大小，以位元組為單位。
-   初始緩衝區飽和度（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




