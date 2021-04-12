---
description: 設定為 IMFOutputSchema 物件的屬性。
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: 'MFPROTECTIONATTRIBUTE_BEST_EFFORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192163"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>MFPROTECTIONATTRIBUTE \_ 最佳 \_ 投入時間屬性

設定為 [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) 物件的屬性。 如果有這個屬性，則會忽略嘗試套用保護的嘗試失敗。 如果相關聯的屬性值為 **TRUE**，則應該套用具有 [MFPROTECTIONATTRIBUTE \_ 故障 \_ 轉移](mfprotectionattribute-fail-over.md) 屬性的保護架構。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

若 **為 TRUE**，如果設定此保護失敗，請使用 [MFPROTECTIONATTRIBUTE \_ 故障 \_ 轉移](mfprotectionattribute-fail-over.md) 屬性來強制執行保護架構。

設定為 [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) 物件的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 UWP 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ UWP 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




