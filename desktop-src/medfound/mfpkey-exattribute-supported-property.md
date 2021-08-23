---
description: 指定媒體基礎轉換 (MFT) 是否將屬性從輸入範例複製到輸出範例。
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: 'MFPKEY_EXATTRIBUTE_SUPPORTED 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663507"
---
# <a name="mfpkey_exattribute_supported-property"></a>MFPKEY \_ EXATTRIBUTE \_ 支援的屬性

指定媒體基礎轉換 (MFT) 是否將屬性從輸入範例複製到輸出範例。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

這個屬性可以具有下列值。



| 值              | 描述                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | MFT 會將屬性從輸入範例複製到輸出範例。                                                                                 |
| **VARIANT \_ FALSE** | 媒體會話會將屬性從輸入範例複製到輸出範例。 它不會覆寫 MFT 在輸出範例上設定的任何屬性。 |



 

若要取得這個屬性，請針對 **IPropertyStore** 介面呼叫 MFT 上的 **QueryInterface** 。

預設值為 **VARIANT \_ FALSE**。 如果 MFT 未公開 **IPropertyStore** 介面，或未設定此屬性，則會將值視為 **VARIANT \_ FALSE**。

這是唯讀的屬性。

> [!NOTE] 
> 這個屬性不會套用到非同步 MFTs。 無論這個屬性的值為何，都不會將屬性從輸入範例複製到非同步 MFTs 的輸出範例。

## <a name="examples"></a>範例

如果 MFT 複製範例屬性，則下列範例會傳回 VARIANT \_ TRUE。


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[**IMFTransform：:P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




