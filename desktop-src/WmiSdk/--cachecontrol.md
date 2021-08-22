---
description: 類別是類別的抽象基類，可用來判斷 WMI 何時應該釋放元件物件模型 (COM) 物件。
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 429e973d83e1f213b011998c75dfbfabd81fb7bb4921f0f8b9f61bcedd6080c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051096"
---
# <a name="__cachecontrol-class"></a>\_\_CacheControl 類別

**\_ \_ CacheControl** 系統類別是類別的抽象基類，可用來判斷 WMI 何時應該釋放元件物件模型 (COM) 物件。 永遠不會建立這個類別的實例。 **\_ \_ CacheControl** 類別只位於根命名空間中。 如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>成員

**\_ \_ CacheControl** 類別不會定義任何成員。

## <a name="remarks"></a>備註

**\_ \_ CacheControl** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_PropertyProviderCacheControl](--propertyprovidercachecontrol.md)
</dt> <dt>

[卸載提供者](unloading-a-provider.md)
</dt> </dl>

 

