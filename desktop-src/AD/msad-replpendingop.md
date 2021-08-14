---
title: MSAD_ReplPendingOp 類別
description: 表示 DS 複寫 \_ 作業 \_ 結構，描述目前正在執行或暫止執行的複寫工作。
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp 類別 Active Directory
- MSAD_ReplPendingOp 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164c5ebe672a52bb399727940e5e51b98904f7db322cc362425dabda25f547a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186073"
---
# <a name="msad_replpendingop-class"></a>MSAD \_ ReplPendingOp 類別

表示 [**DS 複寫 \_ 作業 \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) 結構，描述目前正在執行或暫止執行的複寫工作。 [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)函數會傳回這個結構。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>成員

**MSAD \_ ReplPendingOp** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSAD \_ ReplPendingOp** 類別具有這些屬性。

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得與此作業相關聯之遠端伺服器的傳輸特定網路位址。 如果沒有與這項作業相關聯的遠端伺服器，則 **為 Null** 。

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得與此作業對應的遠端伺服器相關聯的 DSA 的 X-y 路徑。 如果沒有與此作業對應的遠端伺服器，則 **為 Null** 。

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得 **DsaDN** 屬性所識別 DSA 的 [**objectGuid**](/windows/desktop/ADSchema/a-objectguid)屬性值。

</dd> <dt>

**NamingCoNtextDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得與這項作業相關聯之命名內容 (NC) 的 x.500 路徑。

</dd> <dt>

**NamingCoNtextObjGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得 **NamingCoNtextDN** 屬性所識別之 NC 的 [**objectGuid**](/windows/desktop/ADSchema/a-objectguid)屬性。

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得作業開始的時間。 如果這項作業仍在佇列中，則 **為 Null** 。

</dd> <dt>

**選項**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得一組旗標，這些旗標會提供有關作業的其他資料。 此成員的內容是由 **OpType** 屬性的值所決定。

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 同步處理**


</dt> <dd>

包含在 [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)中針對 _Options * 參數定義的一或多個 **DS \_ REPSYNC \_ \** _ 值的零或組合。

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 新增**


</dt> <dd>

包含在 [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)中針對 _Options * 參數定義的一或多個 **DS \_ REPADD \_ \** _ 值的零或組合。

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 刪除**


</dt> <dd>

包含在 [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)中針對 _Options * 參數定義的一或多個 **DS \_ REPDEL \_ \** _ 值的零或組合。

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 修改**


</dt> <dd>

包含在 [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)中針對 _Options * 參數定義的一或多個 **DS \_ REPMOD \_ \** _ 值的零或組合。

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS 複寫作業 \_ \_ \_ 類型 \_ 更新 \_ REFS**


</dt> <dd>

包含在 [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)中針對 _Options * 參數定義的一或多個 **DS \_ REPSUPD \_ \** _ 值的零或組合。

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得 [**DS 複寫 \_ 操作 \_ \_ 類型**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) 值，指出這個類別所代表的作業類型。

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得此作業在佇列中的位置。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得這項作業的優先順序。 較高優先順序的工作會先執行。 優先順序是由伺服器根據此類別所代表的作業類型和作業的參數來計算。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得作業的識別碼，這是每一電腦和每次開機的唯一識別碼。

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得將此作業排入佇列的時間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

