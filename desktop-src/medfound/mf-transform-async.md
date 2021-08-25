---
description: 指定媒體基礎轉換 (MFT) 是否執行非同步處理。
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: 'MF_TRANSFORM_ASYNC 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714347"
---
# <a name="mf_transform_async-attribute"></a>MF \_ 轉換 \_ 非同步屬性

指定媒體基礎轉換 (MFT) 是否執行非同步處理。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

屬性是布林值：

-   如果屬性為非零，則 MFT 會執行非同步處理。
-   如果屬性為0或未設定，則 MFT 為同步。

若要取得這個屬性，請先呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的屬性存放區。 如果該方法成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 來取得屬性值。 如果這兩種方法中的任一個失敗，則 MFT 是同步的。

若為非同步 MFTs，這個屬性必須設定為非零值。 針對同步 MFTs，這個屬性是選擇性的，但如果存在，則必須設定為0。

非同步 MFTs 與舊版媒體基礎不相容。 若要使用非同步 MFT，用戶端必須在 MFT 上設定 [**MF \_ 轉換 \_ 非同步 \_ 解除鎖定**](mf-transform-async-unlock.md) 屬性。  (Microsoft 媒體基礎管線會自動執行此步驟。 ) 

## <a name="examples"></a>範例

下列程式碼會測試 MFT 是否執行非同步處理。


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> <dt>

[**MF \_ 轉換 \_ 非同步 \_ 解除鎖定**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




