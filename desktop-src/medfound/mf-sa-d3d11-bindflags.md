---
description: 指定配置媒體範例的 Microsoft Direct3D 11 介面時所要使用的系結旗標。
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: 'MF_SA_D3D11_BINDFLAGS 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65f0fbc607ccdc8f878e25109fcadfdf8956007d99909d9a21c0e668951106d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102461"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>MF \_ SA \_ D3D11 \_ BINDFLAGS 屬性

指定配置媒體範例的 Microsoft Direct3D 11 介面時所要使用的系結旗標。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 D3D11 系結 [**\_ \_ 旗**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag)標旗標的位 **or** 。

### <a name="microsoft-media-foundation-transforms"></a>Microsoft 媒體基礎轉換

在此內容中，只有當 Microsoft 媒體基礎轉換 (MFT) 針對 [MF \_ SA \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)屬性傳回 **TRUE** 時，才適用此屬性。

如果 MFT 支援 Direct3D 11，則在配置 Microsoft Direct3D 的輸出介面時，這個屬性會提供對 MFT 的提示。 設定屬性，如下所示：

1.  呼叫 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) 以取得 MFT 屬性存放區。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

在串流處理開始之前，媒體基礎管線會設定屬性。 在配置介面時，MFT 應嘗試接受設定。 如果無法這麼做，則 MFT 可以忽略屬性，而不是失敗的配置。

此外，如果 MFT 需要 Direct3D 介面以進行輸入，則可以將此屬性公開為輸入介面如何配置的提示。 查詢屬性，如下所示：

1.  呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 來取得輸入資料流程屬性。
2.  呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

### <a name="sample-allocator"></a>範例配置器

您可以在影片範例配置器的 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) 方法中設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
