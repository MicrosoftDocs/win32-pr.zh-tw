---
description: 指定可識別您要使用之編碼器的 FOURCC。
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: 'MFPKEY_FOURCC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943914"
---
# <a name="mfpkey_fourcc-property"></a>MFPKEY \_ FOURCC 屬性

指定可識別您要使用之編碼器的 FOURCC。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCFOURCC

## <a name="data-type"></a>資料類型

VT \_ I4 (FOURCC 值) 

## <a name="remarks"></a>備註

您必須在使用 **IPropertyBag** 或 **IPropertyStore** 來抓取下列屬性的值之前，先設定此值：

-   [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

您應該使用 [**IWMCodecProps：： GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) 來取出先前所列之 FOURCC 相依屬性的值。 使用 **GetCodecProp** 時，您不需要設定 **MFPKEY \_ FOURCC**。

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

 

 




