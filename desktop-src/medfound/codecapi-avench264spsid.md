---
description: 設定在 SPS 網路抽象層中 (SPS) 識別碼的順序參數集 (NAL) 單位（在 h.264 位串流中）。
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: 'CODECAPI_AVEncH264SPSID 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664658"
---
# <a name="codecapi_avench264spsid-property"></a>CODECAPI \_ AVEncH264SPSID 屬性

設定在 SPS 網路抽象層中 (SPS) 識別碼的順序參數集 (NAL) 單位（在 h.264 位串流中）。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>屬性值

在 SPS NAL 單位中指定 **seq \_ 參數 \_ 集 \_ 識別碼** 的值。 **Seq \_ 參數 \_ 集 \_ 識別碼** 語法元素會識別 sequence 參數集。 產生的位資料流程可以與其他位資料流程串連，以產生較長的位資料流程，其中包含多個具有不同 SPS 識別碼的序列參數集。

有效範圍是 0 31，如 h.264/AVC 規格中所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

