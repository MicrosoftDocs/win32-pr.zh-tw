---
description: 包含的方法可取得視頻電子產品標準關聯之影片輸入定義的原始內容 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 1.x 標準128位元組資料區塊。
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: WmiMonitorDescriptorMethods 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987287"
---
# <a name="wmimonitordescriptormethods-class"></a>WmiMonitorDescriptorMethods 類別

**WmiMonitorDescriptorMethods** WMI 類別包含的方法可取得視頻電子郵件標準關聯之影片輸入定義的原始內容 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 1.x 標準128位元組資料區塊。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>成員

**WmiMonitorDescriptorMethods** 類別具有下列類型的成員：

-   [方法](#wmimonitordescriptormethods-class)
-   [屬性](#properties)

### <a name="methods"></a>方法

**WmiMonitorDescriptorMethods** 類別有這些方法。



| 方法                                                                                           | 描述                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | 存取指定的 EDID 1.x 描述元區塊的原始資料。<br/> |



 

### <a name="properties"></a>屬性

**WmiMonitorDescriptorMethods** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定監視實例的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




