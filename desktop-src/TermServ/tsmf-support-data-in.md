---
title: TSMF_SUPPORT_DATA_IN 結構
description: 包含媒體格式的相關資訊。 |TSMF_SUPPORT_DATA_IN 結構
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN 結構遠端桌面服務
- PTSMF_SUPPORT_DATA_IN 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ae90099b69494425344ff65b73090cce574b843cd1589572203a4786b38ff6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755774"
---
# <a name="tsmf_support_data_in-structure"></a>TSMF \_ 支援 \_ \_ 結構中的資料

包含媒體格式的相關資訊。 在 **WRDS \_ QUERY \_ MF \_ 格式 \_ 支援** 查詢期間， [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)方法會使用此結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>成員

<dl> <dt>

**guidMfSession**
</dt> <dd>

會話。

</dd> <dt>

**numEntries**
</dt> <dd>

變數長度資料中的結構數目。

</dd> <dt>

**...**
</dt> <dd>

包含媒體格式資料之結構的數目不定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>         |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ 支援 \_ NODEDATA \_**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





