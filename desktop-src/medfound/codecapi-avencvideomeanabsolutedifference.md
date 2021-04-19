---
description: 控制 \_ 每個輸出範例上的 MFSampleExtension MeanAbsoluteDifference 透過 IMFAttribute 的信號。
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: 'CODECAPI_AVEncVideoMeanAbsoluteDifference 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986281"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>CODECAPI \_ AVEncVideoMeanAbsoluteDifference 屬性

控制每個輸出範例上的 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 透過 [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 的信號。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>備註

如果應用程式設定非零值，則編碼器應該將 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 範例屬性新增至每個輸出範例。 MFSampleExtension \_ MeanAbsoluteDifference 屬性會指出來源樣本與 Y 平面中預測樣本之間的平均絕對差異。

如果編碼器針對 **GetParameterRange** 傳回0，則編碼器不支援輸出範例上 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 的輸出。

預設值應為0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




