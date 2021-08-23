---
description: 指定編碼期間卸載的影片框架數目。
ms.assetid: e55db53e-ab70-42ce-b5cd-2e59a4e96b7b
title: 'MFPKEY_DROPPEDFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c701399684b15d07ca287813cf6bf9875bab7c17261bb1ae7b9fe2bda2e5254c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663547"
---
# <a name="mfpkey_droppedframes-property"></a>MFPKEY \_ DROPPEDFRAMES 屬性

指定編碼期間卸載的影片框架數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

在編碼期間，有時會略過或捨棄影片框架，因為緩衝區有限制。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
