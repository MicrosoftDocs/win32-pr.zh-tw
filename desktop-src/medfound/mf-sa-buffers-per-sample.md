---
description: 指定影片範例配置器為每個影片範例建立的緩衝區數目。
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: 'MF_SA_BUFFERS_PER_SAMPLE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6b54cc5b2589649c954d9f2f41923af04fdf4aa7c00714067bee0b11dabbee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740365"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>\_ \_ 每個範例的 MF SA 緩衝區 \_ \_ 屬性

指定影片範例配置器為每個影片範例建立的緩衝區數目。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

如果您使用 [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) 介面來配置影片範例，則可以使用此屬性來建立包含多個緩衝區的影片範例。 例如，如果屬性值為2，配置器會為每個影片範例建立兩個影片緩衝區。 在 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)方法的 *pAttributes* 參數中設定屬性。

預設值為 1。 如果未設定屬性，配置器會建立包含每個樣本單一緩衝區的影片範例。

這個屬性主要適用于在下列情況下，媒體基礎轉換 (MFTs 支援身歷聲3D 輸出的) ：

-   MFT 支援 Microsoft DirectX Graphic Infrastructure (DXGI) 。
-   MFT 會配置自己的輸出範例。
-   MFT 會使用 [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) 介面來配置輸出範例。
-   3D 影片格式會針對每個視圖使用不同的緩衝區。

如果上述所有準則都成立，則在每個 view) 中，MFT 應該將屬性值設定為 2 (一個緩衝區。

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

 

 




