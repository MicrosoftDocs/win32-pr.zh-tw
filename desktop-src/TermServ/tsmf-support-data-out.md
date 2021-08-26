---
title: TSMF_SUPPORT_DATA_OUT 結構
description: 包含媒體格式的相關資訊。 |TSMF_SUPPORT_DATA_OUT 結構
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT 結構遠端桌面服務
- PTSMF_SUPPORT_DATA_OUT 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869018"
---
# <a name="tsmf_support_data_out-structure"></a>TSMF \_ 支援 \_ 資料 \_ 輸出結構

包含媒體格式的相關資訊。 在 **WRDS \_ QUERY \_ MF \_ 格式 \_ 支援** 查詢期間， [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)方法會使用此結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>成員

<dl> <dt>

**guidMfSession**
</dt> <dd>

這必須符合結構中對應 [**TSMF \_ 支援 \_ 資料 \_**](tsmf-support-data-in.md)中的 **guidMfSession** 屬性。

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

[**TSMF \_ 支援 \_ NODEDATA \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





