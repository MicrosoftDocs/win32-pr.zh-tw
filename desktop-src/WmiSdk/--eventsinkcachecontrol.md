---
description: 用來判斷 WMI 何時釋放事件取用者提供者 IWbemUnboundObjectSink 指標。
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: dc73e2cb740486ad08172c10233f4865709a87d9f1122f399002133687744094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557912"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_EventSinkCacheControl 類別

**\_ \_ EventSinkCacheControl** 系統類別用來判斷 WMI 何時釋放事件取用者提供者的 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)指標。 **\_ \_ EventSinkCacheControl** 類別是單一類別。 它只位於 \\ 根命名空間中。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>成員

**\_ \_ EventSinkCacheControl** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventSinkCacheControl** 類別具有這些屬性。

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

WMI 釋放事件提供者的時間間隔。 這最多可能需要兩倍的間隔，以卸載提供者。 時間是 [間隔格式](interval-format.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ EventSinkCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。 如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。

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

 

 




