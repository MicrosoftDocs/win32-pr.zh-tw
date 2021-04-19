---
description: 指定 Advanced 系統格式的標記 (ASF) 檔。 這個屬性會對應至 ASF 標頭中定義于 ASF 規格中的標記物件。
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: 'MF_PD_ASF_MARKER 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985350"
---
# <a name="mf_pd_asf_marker-attribute"></a>MF \_ PD \_ ASF \_ 標記屬性

指定 Advanced 系統格式的標記 (ASF) 檔。 這個屬性會對應至 ASF 標頭中定義于 ASF 規格中的標記物件。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從標記物件產生這個屬性。 下表顯示 blob 的格式：



| 標記物件欄位 | 資料類型    | 大小    | Description       |
|---------------------|--------------|---------|-------------------|
| 標記計數       | **Dword**    | 4 個位元組 | 標記數目 |
| 標記             | **位元組**\[\] | 不定  | 標記的陣列  |



 

第一個 **DWORD** 是標記的數目，後面接著標記的陣列。 每個標記都具有下列格式：



| 標記物件欄位       | 資料類型     | 大小    | Description                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| 標記描述長度 | **Dword**     | 4 個位元組 | 描述字串的大小（以位元組為單位），包括 Null 字元。           |
| 標記描述        | **WCHAR**\[\] | 不定  | 描述標記的以 Null 結束的字串。                                 |
| 呈現時間         | **LONGLONG**  | 8 個位元組 | 標記的呈現時間，以 100-毫微秒單位表示。                         |
| 傳送時間                 | **LONGLONG**  | 8 個位元組 | 標記專案的傳送時間（以毫秒為單位）。                                   |
| Offset                    | **UINT64**    | 8 個位元組 | 資料物件中的位移（以位元組為單位），指定市場的位置。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
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

 

 




