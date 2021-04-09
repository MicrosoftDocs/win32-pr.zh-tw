---
description: 當連接器未提供輸出保護時，此屬性會指定 (OTA) 的影片輸出信任授權單位所提供的額外保護。
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: 'MFPROTECTION_CONSTRICTVIDEO_NOOPM 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943737"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM 屬性

當連接器未提供輸出保護時，此屬性會指定 (OTA) 的影片輸出信任授權單位所提供的額外保護。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

這是 (OTA) 的影片輸出信任授權單位所提供的額外保護。當連接器不提供輸出保護時 (請參閱 [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)) 。 在此情況下，OTA 可能會提供這項保護，其效果與 [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) 防護相同。 這是為了避免與先前呼叫 [**IMFOutputPolicy：： GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) 互動造成混淆，其中使用了 MFPROTECTION \_ CONSTRICTVIDEO 保護來協助識別桌面視窗管理員虛擬連接器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




