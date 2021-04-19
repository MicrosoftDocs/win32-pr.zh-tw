---
description: 指定實際包含資料之編解碼器所編碼的影片框架數目。
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: 'MFPKEY_CODEDNONZEROFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987516"
---
# <a name="mfpkey_codednonzeroframes-property"></a>MFPKEY \_ CODEDNONZEROFRAMES 屬性

指定實際包含資料之編解碼器所編碼的影片框架數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

這個值等於 [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) 減去由於位速率限制而捨棄的任何框架，減去任何零位元組的框架。 完成傳遞範例之後，您可以取得此值。 可以為重複的框架建立零位元組的框架。

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

 

 
