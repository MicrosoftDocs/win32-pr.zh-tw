---
description: 代表 CIM SwitchService 物件的透明橋接層面 \_ 。
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848788"
---
# <a name="cim_transparentbridgingservice-class"></a>CIM \_ TransparentBridgingService 類別

代表 [**CIM \_ SwitchService**](cim-switchservice.md) 物件的透明橋接層面。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>成員

**CIM \_ TransparentBridgingService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ TransparentBridgingService** 類別具有這些屬性。

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIB。IETF \| BRIDGE-dot1dTpAgingTime ") 
</dt> </dl>

以秒為單位的超時時間（以秒為單位），用來產生動態學習的轉送資訊。 802.1 D-1990 標準建議預設值300秒。

</dd> <dt>

**裂**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

篩選具有一個以上篩選資料庫的 VLAN 感知參數所使用的資料庫識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ForwardingService**](cim-forwardingservice.md)
</dt> </dl>

 

