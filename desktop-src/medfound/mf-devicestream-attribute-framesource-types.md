---
description: 表示畫面格來源類型。
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: 'MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013188"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>MF \_ DEVICESTREAM \_ 屬性 \_ FRAMESOURCE \_ 類型屬性

表示畫面格來源類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值應該是 [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) 列舉中一或多個值的位元遮罩。 為了支援回溯相容性，當未針對媒體類型定義此屬性時，會假設其值為 **MFFrameSourceTypes：： Color**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1607版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




