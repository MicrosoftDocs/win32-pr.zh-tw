---
description: 指定與端點 DLP 操作相關聯之檔的相關資訊。
title: 'DLP_DOCUMENT_INFO 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495542"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO 結構

指定與端點 DLP 操作相關聯之檔的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>成員

<dl> <dt>

*版本* \[在\]
</dt> <dd>

指定 API 版本的 DWORD。 此值應該一律為 **DLP_DOCUMENT_INFO_V_LATEST**。 此常數定義于「 [端點資料遺失防止](endpointdlp-endpoint-data-loss-prevention.md)」一文中的 endpointdlp 範例頭檔案清單中。

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[在\]
</dt> <dd>

LPCWSTR，指定檔的原始路徑。

</dd> </dl>

<dl> <dt>

*LocalFileName* \[在\]
</dt> <dd>

LPCWSTR，指定檔之實際備份檔案的路徑。

</dd> </dl>



## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |

