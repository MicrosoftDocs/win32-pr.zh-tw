---
description: 包含編解碼器和格式的相關資訊，這些編解碼器和格式是用來將 Advanced 系統格式的內容編碼 (ASF) 檔。 這個屬性會對應到 ASF 標頭中所定義的編解碼器清單物件（在 ASF 規格中定義）。
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: 'MF_PD_ASF_CODECLIST 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c512dee499dbd2d006fb695c89d59add449e64fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471304"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>MF \_ PD \_ ASF \_ CODECLIST 屬性

包含編解碼器和格式的相關資訊，這些編解碼器和格式是用來將 Advanced 系統格式的內容編碼 (ASF) 檔。 這個屬性會對應到 ASF 標頭中所定義的編解碼器清單物件（在 ASF 規格中定義）。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從 ASF 標頭中的編解碼器清單物件產生此屬性。 使用 [ASF 媒體來源](asf-media-source.md) 的應用程式可以藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，然後從呈現描述項取得屬性，來取得這個屬性。

下表顯示內容 blob 的版面配置。



| 編解碼器清單物件欄位 | 資料類型    | 大小    | Description                           |
|-------------------------|--------------|---------|---------------------------------------|
| 編解碼器專案計數     | **DWORD**    | 4 個位元組 | 編解碼器數目                      |
| 編解碼器專案           | **位元組**\[\] | 不定  | 編解碼器資訊結構的陣列 |



 

[程式碼專案] 欄位是結構的陣列。 下表顯示每個專案的格式：




| 編解碼器清單物件欄位 | 資料類型 | 大小 | 描述 | 
|-------------------------|-----------|------|-------------|
| 類型 | <strong>DWORD</strong> | 4 個位元組 | 編解碼器類型。 這個值可以是下列其中一個值：<br /><ul><li>0x0001：音訊編解碼器</li><li>0x0002：影片編解碼器</li><li>0xFFFF：未知</li></ul> | 
| 編解碼器名稱長度 | <strong>DWORD</strong> | 4 個位元組 | 編解碼器名稱字串的大小（以位元組為單位），包括 <strong>Null</strong> 字元。 | 
| 編解碼器名稱 | <strong>WCHAR</strong>[] | 不定 | 以 Null 終止的 Unicode 字串，其中包含編解碼器的名稱，例如 "Windows Media 視訊 9"。 | 
| 編解碼器描述長度 | <strong>DWORD</strong> | 4 個位元組 | 編解碼器描述字串的大小（以位元組為單位），包括 <strong>Null</strong> 字元。 | 
| 編解碼器描述 | <strong>WCHAR</strong>[] | 不定 | 以 null 終止的 Unicode 字串，其中包含編解碼器的描述。 | 
| 編解碼器資訊長度 | <strong>DWORD</strong> | 4 個位元組 | 編解碼器資訊欄位的大小（以位元組為單位）。 | 
| 編解碼器資訊 | <strong>BYTE</strong>[] | 不定 | 編解碼器資料。 這項資料的意義取決於編解碼器。 一般而言，此資料會指出格式。 | 




 

> [!Note]  
> 屬性 blob 的配置與 ASF 標頭中編解碼器清單物件的版面配置不完全相符。 特別是，字串長度會以位元組為單位提供，並包含 **Null** 結束字元的大小。

 

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

 

 




