---
title: TSMF_SUPPORT_NODEDATA_OUT 結構
description: 在 TSMF 內使用 \_ \_ 可支援資料 \_ 輸出結構，以包含支援之媒體格式的相關資訊。
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT 結構遠端桌面服務
- PTSMF_SUPPORT_NODEDATA_OUT 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843840"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ 支援 \_ NODEDATA \_ OUT 結構

在 TSMF 內使用可 [**\_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md) 結構，以包含支援之媒體格式的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>成員

<dl> <dt>

**nodeId**
</dt> <dd>

節點。

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

是否支援 *clsidNewSink* 參數所識別的接收。

可能的值為。

<dt>

0
</dt> <dd>

不支援

</dd> <dt>

1
</dt> <dd>

支援

</dd> </dl>

其他值則為未定義。

</dd> <dt>

**clsidNewSink**
</dt> <dd>

與媒體類型相關聯的接收。

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

接收所支援之媒體類型的以零為基底的索引。

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

[**TSMF \_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md)
</dt> </dl>

 

 





