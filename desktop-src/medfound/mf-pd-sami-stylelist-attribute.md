---
description: 包含已同步處理之可存取媒體交換的易記名稱， (薩米文檔案中定義的薩米) 樣式。
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: 'MF_PD_SAMI_STYLELIST 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852431"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>MF \_ PD \_ 薩米 \_ STYLELIST 屬性

包含已同步處理之可存取媒體交換的易記名稱， (薩米文檔案中定義的薩米) 樣式。

[薩米媒體來源](sami-media-source.md)會在其所建立的表示描述項上設定此屬性。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

屬性 blob 具有下列結構：



資料類型

描述

大小 (位元組)

**Dword**

樣式字串的數目。

4

針對每個樣式字串：

**Dword**

字串的大小（以位元組為單位），包括 **Null** 字元。

4

**LPWSTR**

以 Null 結尾的寬字元字串，其中包含樣式的名稱。

不定



 

若要設定樣式或取得目前的樣式，請使用 [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) 介面。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



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

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[薩米媒體來源](sami-media-source.md)
</dt> </dl>

 

 




