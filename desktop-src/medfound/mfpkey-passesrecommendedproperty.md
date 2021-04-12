---
description: 指定編碼器所支援的最大傳遞數目。
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: 'MFPKEY_PASSESRECOMMENDED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192249"
---
# <a name="mfpkey_passesrecommended-property"></a>MFPKEY \_ PASSESRECOMMENDED 屬性

指定編碼器所支援的最大傳遞數目。 唯讀。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCPassesRecommended、g \_ wszWMCPMaxPasses

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

您可以取得這個屬性的值，呼叫 [IWMCodecProps：： GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)。 如果您使用 **IPropertyBag**，您必須先使用 [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md) 屬性來設定所需壓縮格式的 FOURCC 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




