---
description: ASF 媒體接收器的基底傳送時間（以毫秒為單位）。
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: 'MFPKEY_ASFMEDIASINK_BASE_SENDTIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992639"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME 屬性

ASF 媒體接收器的基底傳送時間（以毫秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>備註

傳送時間是在網路上傳送 ASF 封包的時間。 它不會直接對應至封包中資料的呈現時間。

您可以使用這個屬性來設定 ASF 媒體接收器。 使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




