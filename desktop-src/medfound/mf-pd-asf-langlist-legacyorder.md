---
description: 包含目前簡報中使用的 RFC 1766 語言清單。
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: 'MF_PD_ASF_LANGLIST_LEGACYORDER 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102928"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER 屬性

包含目前簡報中使用的 RFC 1766 語言清單。

## <a name="data-type"></a>資料類型

**位元組 \[\]**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="applies-to"></a>適用於

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>備註

這個屬性會套用至透過呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)從 [ASF ContentInfo 物件](asf-contentinfo-object.md)產生的呈現描述項。 位元組陣列的格式如下所示：



| 語言清單物件欄位 | 資料類型    | 大小    | 描述                            |
|----------------------------|--------------|---------|----------------------------------------|
| 語言識別項記錄計數  | **DWORD**    | 4 個位元組 | 語言數目                    |
| 語言識別項記錄        | **位元組**\[\] | 不定  | 語言字串的陣列 (請參閱下面的) 。 |



 

第一個 **DWORD** 是語言的數目，後面接著語言識別項字串的陣列。 每個字串的格式如下：



| 語言清單物件欄位 | 資料類型     | 大小    | 描述                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| 語言識別項長度         | **DWORD**     | 4 個位元組 | 字串的長度（以位元組為單位），包括尾端 **Null** 字元的大小。 |
| 語言識別碼                | **WCHAR**\[\] | 不定  | 以 null 終止的字串，包含 RFC 1766 語言名稱。                           |



 

每個字串都是符合 RFC 1766 的語言標記。

使用這個屬性的目的，只是為了與 Windows 媒體格式 SDK 中 [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)介面的列舉順序保持相容。 語言字串會以不同的順序儲存在 [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) 屬性中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
