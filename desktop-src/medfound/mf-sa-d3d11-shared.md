---
description: 指示影片範例配置器使用索引 mutex 將材質建立為可共用。
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: 'MF_SA_D3D11_SHARED 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 439e92ca57c306434898bfe167646d4e9df98a4cee0b4db8b9c8f84e394cdc21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875979"
---
# <a name="mf_sa_d3d11_shared-attribute"></a>MF \_ SA \_ D3D11 \_ 共用屬性

指示影片範例配置器使用索引 mutex 將材質建立為可共用。

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

[未搭配 MUTEX 的 MF \_ SA \_ D3D11 \_ 共用 \_ \_](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




