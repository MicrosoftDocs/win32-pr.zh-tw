---
description: 控制何時卸載事件提供者。
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d027fec5aea132524924655047c0f0a8aa8605d1972c6f91b2c2315c5834ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557922"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_EventProviderCacheControl 類別

**\_ \_ EventProviderCacheControl** 系統類別會控制何時卸載事件提供者。 它只位於 \\ 根命名空間中。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>成員

**\_ \_ EventProviderCacheControl** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventProviderCacheControl** 類別具有這些屬性。

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

Windows Management Instrumentation (WMI) 釋放事件提供者之後的時間間隔。 時間是 [間隔格式](interval-format.md)。 最多可能需要指定間隔兩倍來卸載提供者。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ EventProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。

如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | Root<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

