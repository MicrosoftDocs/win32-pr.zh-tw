---
title: MDM_DeviceManageability_Provider01_01 類別
description: MDM \_ DeviceManageability \_ Provider01 \_ 01 類別可用來取得裝置上 mdm 設定功能的一般資訊。
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- MDM_DeviceManageability_Provider01_01 類別
- MDM_DeviceManageability_Provider01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843968"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a>MDM \_ DeviceManageability \_ Provider01 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ DeviceManageability \_ Provider01 \_ 01 類別可用來取得裝置上 mdm 設定功能的一般資訊。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a>成員

**MDM \_ DeviceManageability \_ Provider01 \_ 01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ DeviceManageability \_ Provider01 \_ 01** 類別具有這些屬性。

<dl> <dt>

[ConfigInfo](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

您必須將值設定為 [WMI \_ Bridge \_ 伺服器]。 呼叫端無法動態設定提供者識別碼。

</dd> <dt>

[EnrollmentInfo](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
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

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

