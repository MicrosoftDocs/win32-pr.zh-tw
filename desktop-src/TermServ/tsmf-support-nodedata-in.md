---
title: TSMF_SUPPORT_NODEDATA_IN 結構
description: 在 TSMF 中使用 \_ ， \_ \_ 可支援結構中的資料，以包含支援之媒體格式的相關資訊。
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN 結構遠端桌面服務
- PTSMF_SUPPORT_NODEDATA_IN 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755720"
---
# <a name="tsmf_support_nodedata_in-structure"></a>\_ \_ \_ 結構中的 TSMF 支援 NODEDATA

在 TSMF 中使用，可 [**\_ 支援結構 \_ \_ 中的資料**](tsmf-support-data-in.md) ，以包含支援之媒體格式的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>成員

<dl> <dt>

**byteCount**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**nodeId**
</dt> <dd>

節點。

</dd> <dt>

**numMediaTypes**
</dt> <dd>

媒體格式結構的數目。

</dd> <dt>

**...**
</dt> <dd>

定義音訊或影片媒體格式的結構數目不定。 **FormatType** 可為音訊 **格式化 \_ WaveFormatEx** 或影片的 **格式 \_ MFVideoFormat** 。

如需此結構的詳細資訊，請參閱 [TS \_ AM \_ 媒體 \_ 類型結構](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934)。

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

[**TSMF \_ \_ \_ 中的支援資料**](tsmf-support-data-in.md)
</dt> </dl>

 

