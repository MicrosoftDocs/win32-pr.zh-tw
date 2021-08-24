---
description: 指定與端點 DLP 列印操作相關聯之檔的相關資訊。
title: 'DLP_PRINT_INFO 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e55b3dc22c77d85e15499ea0fb2a6634ece044496637c811ae42e4afd632704e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725818"
---
# <a name="dlp_print_info-structure"></a>DLP_PRINT_INFO 結構

指定與端點 DLP 列印操作相關聯之檔的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>成員

<dl> <dt>

*版本* \[在\]
</dt> <dd>

指定 API 版本的 DWORD。 此值應該一律為 **DLP_PRINT_INFO_V_LATEST**。 此常數定義于「 [端點資料遺失防止](endpointdlp-endpoint-data-loss-prevention.md)」一文中的 endpointdlp 範例頭檔案清單中。

</dd> </dl>

<dl> <dt>

*PrinterName* \[在\]
</dt> <dd>

識別目的地印表機的 LPCWSTR。

</dd> </dl>

<dl> <dt>

*JobName* \[在\]
</dt> <dd>

指定列印工作名稱的 LPCWSTR。

</dd> </dl>

<dl> <dt>

*OutputFileName* \[在\]
</dt> <dd>

LPCWSTR，指定輸出檔案在列印至檔案時的路徑。

</dd> </dl>



## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |

