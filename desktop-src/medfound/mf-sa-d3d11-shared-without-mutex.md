---
description: 指示影片範例配置器使用舊版機制，將材質建立為可共用。
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: 'MF_SA_D3D11_SHARED_WITHOUT_MUTEX 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8495d0c2033f6ffbc1a212c9768af3157697eb588c968cb3fbd62959fa3515f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740299"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a>\_未搭配 \_ \_ \_ \_ MUTEX 屬性共用的 MF SA D3D11

指示影片範例配置器使用舊版機制，將材質建立為可共用。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

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
</dt> <dt>

[**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[MF \_ SA \_ D3D11 \_ 共用](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




