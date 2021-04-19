---
description: 範例抓取程式收到的每個樣本上的時間戳記之間的位移，以及範例抓取器呈現範例的時間。
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: 'MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979743"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET 屬性

範例抓取程式收到的每個樣本上的時間戳記之間的位移，以及範例抓取器呈現範例的時間。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

您可以在 [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)物件上設定這個屬性。 這個屬性可讓範例抓取器的回呼函式接收比展示時間更早的範例。

當範例抓取器收到新的範例時，它會在 time *t* − *offset* 上顯示範例，其中 *t* 是樣本上的時間戳記，而 *offset* 是這個屬性的值。 如果未設定此屬性，則預設值為零。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 




