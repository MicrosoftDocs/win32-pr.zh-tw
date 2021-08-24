---
title: MDM_SharedPC 類別
description: MDM \_ >sharedpc 類別是用來設定共用電腦使用方式的設定。
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- MDM_SharedPC 類別
- MDM_SharedPC 類別，描述
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d4888e0d8129584e79124079e93459bc6d9f963fe026704f52b34de05b755e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693458"
---
# <a name="mdm_sharedpc-class"></a>MDM \_ >sharedpc 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ >sharedpc 類別是用來設定共用電腦使用方式的設定。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a>成員

**MDM \_ >sharedpc** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ >sharedpc** 類別具有這些屬性。

<dl> <dt>

[AccountModel](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[DeletionPolicy](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[DiskLevelCaching](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[DiskLevelDeletion](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[EnableAccountManager](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[EnableSharedPCMode](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[InactiveThreshold](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

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

[KioskModeAUMID](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[KioskModeUserTileDisplayText](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[MaintenanceStartTime](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[MaxPageFileSizeMB](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RestrictLocalStorage](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[SetEduPolicies](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[SetPowerPolicies](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[SignInOnResume](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> <dt>

[SleepTimeout](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

