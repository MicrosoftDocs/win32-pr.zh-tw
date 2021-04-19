---
description: ASF 屬性
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: ASF 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973597"
---
# <a name="asf-attributes"></a>ASF 屬性

### <a name="profile-attributes"></a>配置檔案屬性

下列屬性適用于 ASF 設定檔。



| 屬性                                                                      | 描述                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | 指定 ASF 檔案的封包大小上限（以位元組為單位）。 |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | 指定 ASF 檔案的最小封包大小（以位元組為單位）。 |



 

### <a name="stream-configuration-attributes"></a>串流設定屬性

下列屬性適用于 ASF 資料流程設定物件。



| 屬性                                                                              | 描述                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | 設定用來編碼 Windows Media 檔案的平均 "有漏洞 bucket" 參數。 |
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | 設定用來編碼 Windows Media 檔案的尖峰 "有漏洞 bucket" 參數。    |



 

### <a name="media-buffer-attributes"></a>媒體緩衝區屬性

下列屬性適用于 ASF 封包的媒體緩衝區。



| 屬性                                                                          | 描述                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**MFASFSPLITTER 封 \_ 包 \_ 界限**](mfasfsplitter-packet-boundary-attribute.md) | 指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。 |



 

### <a name="presentation-descriptor-attributes"></a>展示描述項屬性

如需適用于 ASF 表示描述項的屬性清單，請參閱 [展示描述項屬性](presentation-descriptor-attributes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



