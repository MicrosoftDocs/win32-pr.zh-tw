---
description: 指定 ASF 媒體接收器是否自動調整位元速率。
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: 'MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998948"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率屬性

指定 ASF 媒體接收器是否自動調整位元速率。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

如果這個屬性的值為 VARIANT \_ ，則 asf 媒體接收器會自動調整 asf 內容的位元速率，以回應多工處理的資料流程特性。

這個屬性會影響當資料流程溢出接收的 "有漏洞 bucket" 參數時，ASF 媒體接收器的行為：



| 值              | 行為                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | ASF 媒體接收器會自動調整 ASF 內容的位元速率，以回應多工處理的資料流程特性。 |
| **VARIANT \_ FALSE** | ASF 媒體接收器會使用應用程式所提供的資料流程位元速率值。                                                                |



 

預設值為 **VARIANT \_ FALSE**。

當您設定 ASF 媒體接收時，請設定此屬性。 使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。

將此屬性設定為 VARIANT \_ TRUE 會導致 asf 媒體接收器在 asf 多工器上設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標。 請參閱 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags)。

如需有關有漏洞 bucket 概念的詳細資訊，請參閱 Windows Media Format SDK 檔中的「有漏洞 Bucket 緩衝區模型」主題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




