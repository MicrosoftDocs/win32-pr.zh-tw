---
title: IMsRdpExtendedSettings 介面
description: 用來設定和取出用戶端控制項的命名屬性。
ms.assetid: b78eebc1-e514-4201-becf-770ee4a15187
ms.tgt_platform: multiple
keywords:
- IMsRdpExtendedSettings 介面遠端桌面服務
- IMsRdpExtendedSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ec34087b7bb6e943029cb6051a91b30d1ba5e40f01f6cb620735ceb0d14e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058896"
---
# <a name="imsrdpextendedsettings-interface"></a>IMsRdpExtendedSettings 介面

用來設定和取出用戶端控制項的命名屬性。

## <a name="members"></a>成員

**IMsRdpExtendedSettings** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpExtendedSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpExtendedSettings** 介面具有這些屬性。



| 屬性                                                       | 存取類型           | 描述                           |
|:---------------------------------------------------------------|:----------------------|:--------------------------------------|
| [**屬性**](imsrdpextendedsettings-property.md)<br/> | 讀取/寫入<br/> | 包含已命名的屬性。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings 定義為302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                                                                                                                            |



 

