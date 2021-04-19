---
description: 指定此解碼器的電源等級。
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: 'MFPKEY_AVDecVideoSWPowerLevel 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974525"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>MFPKEY \_ AVDecVideoSWPowerLevel 屬性

指定此解碼器的電源等級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="default-value"></a>預設值

**100**

## <a name="remarks"></a>備註

這個屬性必須設定為下列其中一個值。



| 值 | 意義                                                             |
|-------|---------------------------------------------------------------------|
| 0     | 此解碼器使用已針對電池壽命優化的電源等級。  |
| 50    | 此解碼器使用平衡的電源等級。                            |
| 100   | 此解碼器會使用針對影片品質優化的電源等級。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
