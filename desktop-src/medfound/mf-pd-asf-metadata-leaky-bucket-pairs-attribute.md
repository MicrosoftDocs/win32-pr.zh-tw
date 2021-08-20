---
description: 為變數位元速率指定位速率和對應緩衝區視窗的清單， (VBR) Advanced 系統格式 (ASF) 檔。
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: 'MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9444292ad437551622e1f418a6f21198ecd8341f01e4e5bda0a2047f847cfd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740746"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>MF \_ PD \_ ASF \_ 中繼資料 \_ 有漏洞 \_ BUCKET \_ 配對屬性

為變數位元速率指定位速率和對應緩衝區視窗的清單， (VBR) Advanced 系統格式 (ASF) 檔。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，此屬性會套用至 ASF 內容的表示描述項。

屬性值的格式如下：

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

**WM \_ 有漏洞 \_ BUCKET \_** 組結構的定義如下：

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

針對每個位元速率， **msBufferWindow** 成員會指出播放開始之前要緩衝的內容量（以毫秒為單位）。 緩衝區的大小（以位元組為單位）等於 **msBufferWinow** x **dwBitrate** /8000。

> [!Note]  
> 這個屬性會對應至 Windows 媒體格式 SDK 中的 **ASFLeakyBucketPairs** 屬性。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




