---
title: " (Fwpmu) 存取右邊識別碼"
description: Windows 篩選平台 (WFP) 使用標準的 Win32 存取權限，以及一組在篩選平臺內建的 WFP 特定存取權限。
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935047"
---
# <a name="access-right-identifiers"></a>存取正確的識別碼

Windows 篩選平台 (WFP) 使用 [標準的 Win32 存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及一組在篩選平臺內建的 WFP 特定存取權限。 只有在使用者模式下，才會使用這些存取權限來保護物件的安全。 核心模式呼叫端略過所有存取檢查。

WFP 特定的存取權限識別碼如下所示。

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ 新增**
</dt> <dd> <dl> <dt>



將物件新增至基底篩選引擎 (BFE) 。 需要有此存取權限，才能呼叫 [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) 函數。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ 新增 \_ 連結**
</dt> <dd> <dl> <dt>



新增透過連結所參考的物件。 例如，透過 Guid 參考的標注需要此存取權。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN**
</dt> <dd> <dl> <dt>



開始唯讀交易。 需要此存取權限才能呼叫 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN**
</dt> <dd> <dl> <dt>



開始讀取/寫入交易。 需要有此存取權限，才能呼叫 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) 進行讀取/寫入交易。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ 分類**
</dt> <dd> <dl> <dt>



將遠端程序呼叫分類 (RPC) 。 RPC 執行時間需要此存取權，才能強制執行 RPC 篩選器。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ 列舉**
</dt> <dd> <dl> <dt>



枚舉。 需要有此存取權限，才能呼叫 [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) 函數。 若要列舉物件，呼叫端也需要 \_ \_ 物件的 FWPM ACTRL READ 存取權。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**
</dt> <dd> <dl> <dt>



開啟篩選引擎的會話。 需要此存取權限才能呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**
</dt> <dd> <dl> <dt>



讀取。 需要有此存取權限，才能呼叫 [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) 和 [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) 函數。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**
</dt> <dd> <dl> <dt>



讀取統計資料。 需要有此存取權限，才能呼叫 [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) 和 [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ 訂閱**
</dt> <dd> <dl> <dt>



訂閱。 需要有此存取權限，才能呼叫 [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) 函數。 若要接收物件的通知，訂閱者也需要 \_ \_ 物件的 FWPM ACTRL READ 存取權。


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ 寫入**
</dt> <dd> <dl> <dt>



撰寫引擎選項。 需要此存取權限才能呼叫 [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)。


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM \_ 一般 \_ 讀取**
</dt> <dd> <dl> <dt>



標準 \_ 許可權 \_ 讀取 \| FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN \| FWPM \_ ACTRL \_ 分類 \| FWPM \_ ACTRL \_ 開啟 \| FWPM \_ ACTRL \_ 讀取 \| FWPM \_ ACTRL \_ 讀取 \_ 統計資料


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM \_ 一般 \_ 執行**
</dt> <dd> <dl> <dt>



標準 \_ RIGHTS \_ EXECUTE \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ 訂閱


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM \_ 一般 \_ 寫入**
</dt> <dd> <dl> <dt>



標準 \_ 許可權 \_ 寫入 \| 刪除 \| FWPM \_ ACTRL \_ 新增 \| FWPM \_ ACTRL \_ 新增 \_ 連結 \| FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN \| \_ \_ FWPM ACTRL 寫入


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ 泛型 \_ 全部**
</dt> <dd> <dl> <dt>



標準 \_ 許可權 \_ 需要 \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD \_ LINK \| FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN \| FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN \| FWPM \_ ACTRL FWPM ACTRL \_ \| \_ FWPM \_ ENUM \| ACTRL \_ FWPM \_ OPEN \| ACTRL \_ FWPM \_ READ \| ACTRL \_ FWPM \_ READ \_ STATS \| ACTRL \_ FWPM \_ 訂閱 \| ACTRL \_ \_ WRITE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows 篩選平台存取控制模型](access-control.md)
</dt> <dt>

[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

