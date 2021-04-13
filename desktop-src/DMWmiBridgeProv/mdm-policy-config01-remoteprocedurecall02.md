---
title: MDM_Policy_Config01_RemoteProcedureCall02 類別
description: MDM \_ Policy \_ Config01 RemoteProcedureCall02 類別會設定 \_ 遠端程序呼叫原則。
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- MDM_Policy_Config01_RemoteProcedureCall02 類別
- MDM_Policy_Config01_RemoteProcedureCall02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1c1a188afd3694273080c6c369a8dc37abb22a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465233"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a>MDM \_ 原則 \_ Config01 \_ RemoteProcedureCall02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ Policy \_ Config01 RemoteProcedureCall02 類別會設定 \_ 遠端程序呼叫原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Config01 \_ RemoteProcedureCall02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Config01 \_ RemoteProcedureCall02** 類別具有這些屬性。

<dl> <dt>

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

</dd> <dt>

[RestrictUnauthenticatedRPCClients](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RPCEndpointMapperClientAuthentication](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

