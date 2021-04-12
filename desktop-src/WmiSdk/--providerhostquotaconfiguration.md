---
description: 允許在主機進程使用系統資源時設定限制。
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193067"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_ProviderHostQuotaConfiguration 類別

**\_ \_ ProviderHostQuotaConfiguration** 系統類別是主機提供者進程的設定類別。 此類別位於根命名空間中，並允許在主機進程使用系統資源時設定限制。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>成員

**\_ \_ ProviderHostQuotaConfiguration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ ProviderHostQuotaConfiguration** 類別具有這些屬性。

<dl> <dt>

**HandlesPerHost**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

每個主機可以有的核心物件控制碼數目。

</dd> <dt>

**MemoryAllHosts**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

所有主機可以保留的私用記憶體（以位元組為單位）組合。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**MemoryPerHost**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

每部主機可以保留的私用記憶體數量。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**ProcessLimitAllHosts**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

可以同時執行的主控制項進程總數。

</dd> <dt>

**ThreadsPerHost**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

任何一部主機擁有的執行緒數目。

</dd> </dl>

## <a name="remarks"></a>備註

代表限制的屬性可以變更，但因為此類別是單一類別，所以所有提供者主機都會共用相同的限制。

設定主機工作物件的工作物件限制時，會使用下列參數：

-   **MemoryAllHosts**
-   **MemoryPerHost**
-   **ProcessLimitAllHosts**
-   **ThreadsPerHost**

如果違反 **HandlesPerHost** 配額，主機進程會輪詢處理常式的使用，並結束進程。 這些值的變更會在電腦重新開機之後生效。

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
</dt> </dl>

 

