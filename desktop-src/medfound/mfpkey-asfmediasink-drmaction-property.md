---
description: 指定如何將 ASF 媒體接收器套用 Windows 媒體 DRM。
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: 'MFPKEY_ASFMEDIASINK_DRMACTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874342"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>MFPKEY \_ ASFMEDIASINK \_ DRMACTION 屬性

指定如何將 ASF 媒體接收器套用 Windows 媒體 DRM。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>備註

這個屬性的值是 [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) 列舉的成員。

您可以使用這個屬性來設定 ASF 媒體接收器。 使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
