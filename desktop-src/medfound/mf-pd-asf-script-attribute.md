---
description: 指定指令碼命令清單以及 Advanced 系統格式的參數 (ASF) 檔。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的指令碼命令物件。
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: 'MF_PD_ASF_SCRIPT 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987236"
---
# <a name="mf_pd_asf_script-attribute"></a>MF \_ PD \_ ASF \_ 腳本屬性

指定指令碼命令清單以及 Advanced 系統格式的參數 (ASF) 檔。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的指令碼命令物件。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從指令碼命令物件標頭產生此屬性。 下表顯示 blob 的格式：



| 指令碼命令物件欄位 | 資料類型    | 大小    | Description               |
|-----------------------------|--------------|---------|---------------------------|
| 命令計數              | **Dword**    | 4 個位元組 | 指令碼命令數目 |
| 命令類型，命令      | **位元組**\[\] | 不定  | 指令碼命令陣列  |



 

第一個 **DWORD** 是指令碼命令的數目，後面接著命令陣列。 每個指令碼命令都具有下列格式：



| 指令碼命令物件欄位 | 資料類型     | 大小    | Description                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| 命令名稱長度         | **Dword**     | 4 個位元組 | 命令字串的大小（以位元組為單位），包括 Null 字元。      |
| 命令名稱：                | **WCHAR**\[\] | 不定  | 以 Null 終止的字串，其中包含指令碼命令。                 |
| 命令類型名稱長度    | **Dword**     | 4 個位元組 | 命令類型字串的大小（以位元組為單位），包括 Null 字元。 |
| 命令類型名稱           | **WCHAR**\[\] | 不定  | 以 Null 終止的字串，其中包含命令類型。                   |
| 呈現時間           | **Dword**     | 4 個位元組 | 命令的呈現時間（以毫秒為單位）。                        |



 

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

 

 




