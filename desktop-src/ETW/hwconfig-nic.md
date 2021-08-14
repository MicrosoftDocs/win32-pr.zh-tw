---
description: HWConfig \_ NIC 類別是網路介面卡設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394722"
---
# <a name="hwconfig_nic-class"></a>HWConfig \_ NIC 類別

**HWConfig \_ NIC** 類別是網路介面卡設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>成員

**HWConfig \_ NIC** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**HWConfig \_ NIC** 類別具有這些屬性。

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

網路介面卡的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




