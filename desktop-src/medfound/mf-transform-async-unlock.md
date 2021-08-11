---
description: 啟用使用非同步媒體基礎轉換 (MFT) 。
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: 'MF_TRANSFORM_ASYNC_UNLOCK 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244174"
---
# <a name="mf_transform_async_unlock-attribute"></a>MF \_ 轉換 \_ 非同步 \_ 解除鎖定屬性

啟用使用非同步媒體基礎轉換 (MFT) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

非同步 MFTs 與舊版 Microsoft 媒體基礎不相容。 若要防止現有的應用程式不小心使用非同步 MFT，必須先將此屬性設定為非零值，才能使用非同步 MFT。 媒體基礎管線會自動設定屬性，因此大部分的應用程式不需要使用此屬性。 但是，如果應用程式使用媒體基礎管線以外的非同步 MFT，則應用程式必須設定這個屬性。

同步 MFTs 不需要此屬性。

若要測試 MFT 是否為非同步，請在 MFT 上取得 [MF \_ 轉換 \_ ASYNC](mf-transform-async.md) 屬性的值。

## <a name="examples"></a>範例

下列程式碼會解除鎖定非同步 MFT。


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
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
</dt> </dl>

 

 




