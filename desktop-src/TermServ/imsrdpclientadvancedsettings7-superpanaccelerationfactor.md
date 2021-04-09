---
title: IMsRdpClientAdvancedSettings7 SuperPanAccelerationFactor 屬性
description: 指定或抓取表示 SuperPan 加速因素的值。 SuperPan 加速因素決定在 SuperPan 模式下，螢幕的移動速度。
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- SuperPanAccelerationFactor 屬性遠端桌面服務
- SuperPanAccelerationFactor 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，SuperPanAccelerationFactor 屬性
- SuperPanAccelerationFactor 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，SuperPanAccelerationFactor 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935135"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>IMsRdpClientAdvancedSettings7：： SuperPanAccelerationFactor 屬性

指定或抓取表示 SuperPan 加速因素的值。 SuperPan 加速因素決定在 SuperPan 模式下，螢幕的移動速度。 加速因數是在用戶端的每個滑鼠移動圖元的指定方向，螢幕視圖所滾動的圖元數。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>屬性值

要設定的 SuperPan 加速因素。 SuperPan 加速因素是螢幕視圖在每個滑鼠移動圖元的指定方向滾動的圖元數。

## <a name="remarks"></a>備註

如需 SuperPan 的詳細資訊，請參閱 [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





