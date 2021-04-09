---
title: IMsRdpClientAdvancedSettings7 EnableSuperPan 屬性
description: 指定或抓取布林值，指出 SuperPan 是否已啟用或停用。
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- EnableSuperPan 屬性遠端桌面服務
- EnableSuperPan 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableSuperPan 屬性
- EnableSuperPan 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableSuperPan 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686066"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>IMsRdpClientAdvancedSettings7：： EnableSuperPan 屬性

指定或抓取布林值，指出 SuperPan 是否已啟用或停用。 SuperPan 是一項功能，可讓使用者在遠端桌面的維度大於目前用戶端視窗的維度時，輕鬆地在全螢幕模式下流覽遠端桌面。 使用者可以指向視窗框線，而不是使用捲軸來流覽桌面，而是讓遠端桌面自動在該方向中滾動。 SuperPan 不支援一個以上的監視器。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>屬性值

**VARIANT \_ BOOL** 值，指定是否啟用 SuperPan。 **VARIANT \_ TRUE** 值指定啟用 SuperPan。

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
</dt> </dl>

 

 





