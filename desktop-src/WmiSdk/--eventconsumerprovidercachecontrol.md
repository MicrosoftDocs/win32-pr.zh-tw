---
description: 決定 WMI 何時應該釋放事件取用者提供者。
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981693"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_EventConsumerProviderCacheControl 類別

**\_ \_ EventConsumerProviderCacheControl** 系統類別會決定 WMI 何時應該釋放事件取用者提供者。 **\_ \_ EventConsumerProviderCacheControl** 類別是單一類別。 它只位於 \\ 根命名空間中。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>成員

**\_ \_ EventConsumerProviderCacheControl** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventConsumerProviderCacheControl** 類別具有這些屬性。

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

WMI 釋放事件取用者提供者之前的時間間隔。 最多可能需要指定間隔兩倍來卸載提供者。 時間是 [間隔格式](interval-format.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ EventConsumerProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。 如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | Root<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

 




