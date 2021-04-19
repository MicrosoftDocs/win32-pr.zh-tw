---
description: 指定本機外掛程式控制原則。
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: 'MF_LOCAL_PLUGIN_CONTROL_POLICY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999952"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>MF \_ 本機 \_ 外掛程式 \_ 控制 \_ 原則屬性

指定本機外掛程式控制原則。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

將此屬性設定為其中一個 [**MF \_ 外掛程式 \_ 控制 \_ 原則**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) 值。

此屬性可讓應用程式指定比 [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)所設定的整個進程原則更嚴格的本機原則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




