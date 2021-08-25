---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別
description: MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02 類別是用來抓取 StartTime 和 StopTime 中存在的記錄。
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c307f2b5ddcad1631cd5981a0ea25d8b9fb43566a482de20a2d050a0f3e8db57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913570"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>MDM \_ 報告 \_ SecurityAuditing01 \_ RetrieveByTimeRange02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別用來抓取 starttime 和 StopTime 中的記錄檔。 STARTTIME 和 StopTime 是以 ISO 8601 格式表示。 如果未指定 StartTime 和 StopTime，則會將值轉譯為第一個現有或最後一個現有的時間。

以下是其他可能的案例：

-   如果未指定 StartTime 和 StopTime，則會傳回所有現有的記錄。
-   如果指定了 StopTime，但未指定 StartTime，則會傳回 StopTime 之前存在的所有記錄。
-   如果指定 StartTime，但是未指定 StopTime，則會傳回從 StartTime 中存在的所有記錄。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a>成員

**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。 此類別的字串為 "RetrieveByTimeRange"。

</dd> <dt>

[記錄](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/SecurityAuditing"

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                            |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mof \\DMWmiBridgeProv.dll</dt> </dl> |



 

