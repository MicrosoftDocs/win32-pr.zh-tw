---
title: MSAD_ReplNeighbor 類別的 SyncNamingCoNtext 方法
description: 呼叫 DsReplicaSync 函式，此函式會將目的地命名內容與其中一個來源進行同步處理。
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- SyncNamingCoNtext 方法 Active Directory
- SyncNamingCoNtext 方法 Active Directory，MSAD_ReplNeighbor 類別
- MSAD_ReplNeighbor 類別 Active Directory，SyncNamingCoNtext 方法
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024666"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>MSAD ReplNeighbor 類別的 SyncNamingCoNtext 方法 \_

呼叫 [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) 函式，此函式會將目的地命名內容與其中一個來源進行同步處理。

## <a name="syntax"></a>語法


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*選項* \[在\]
</dt> <dd>

決定方法如何處理要求的其他資料。 這個參數可以是下列值的組合。

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS \_ REPSYNC \_ 新增 \_ 參考**


</dt> <dd>

導致來源目錄服務代理程式 (DSA) 驗證 [來源複寫至] 清單中是否有本機 DSA。 如果未出現本機 DSA，則會新增它。 這可確保來源傳送變更通知。

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ 所有 \_ 來源**


</dt> <dd>

不支援這個值。

**Windows server 2008 R2、Windows Server 2008 和 Windows Server 2003：** 從所有來源進行同步處理。

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS \_ REPSYNC \_ 非同步 \_ 操作**


</dt> <dd>

以非同步方式執行此作業。

**Windows server 2008 R2、Windows Server 2008 和 Windows Server 2003：** 使用 **DS \_ REPSYNC \_ 所有 \_ 來源** 時的必要。

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ REPSYNC \_ 強制**


</dt> <dd>

即使連結目前已停用，也會進行同步處理。

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC 已 \_ 滿**


</dt> <dd>

從第一個更新序號開始同步處理 (USN) 。

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS \_ REPSYNC 網站 \_ 間 \_ 訊息**


</dt> <dd>

使用 ISM 進行同步處理。

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ 沒有 \_ 捨棄**


</dt> <dd>

不捨棄此同步處理要求，即使類似的同步處理已暫止也一樣。

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ 定期**


</dt> <dd>

指出此作業是由系統管理員排程的定期同步處理要求。

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ 緊急**


</dt> <dd>

指出此作業是標示為緊急更新的通知。

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC 可 \_ 寫入**


</dt> <dd>

表示這個複本是可寫入的。 如果未設定此旗標，則複本會是唯讀的。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





