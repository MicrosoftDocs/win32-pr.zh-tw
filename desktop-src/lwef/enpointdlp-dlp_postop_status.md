---
description: 指定有關端點 DLP 操作的狀態資訊。
title: 'DLP_POSTOP_STATUS 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610228"
---
# <a name="dlp_postop_status-structure"></a>DLP_POSTOP_STATUS 結構

指定有關端點 DLP 操作的狀態資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>成員

<dl> <dt>

*版本* \[在\]
</dt> <dd>

指定 API 版本的 DWORD。 此值應該一律為 **DLP_POSTOP_STATUS_V_LATEST**。 此常數定義于[端點資料遺失預防措施](endpointdlp-endpoint-data-loss-prevention.md)中的 endpointdlp 範例頭檔案清單中

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[在\]
</dt> <dd>

布林值，指出開啟作業是否成功。

</dd> </dl>





## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
