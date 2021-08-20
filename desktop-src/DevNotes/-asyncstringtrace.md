---
description: AsyncStringTrace 函式-完成使用 sprintf 樣式追蹤的選擇性欄位來設定追蹤緩衝區。
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: ac099b0b69c1417c428aefe04b8e6591f945545a2b69196da588ebce8de23f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076172"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace 函式

完成使用 **sprintf** 樣式追蹤的選擇性欄位來設定追蹤緩衝區。

## <a name="syntax"></a>語法


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

用於應用層級篩選的32位追蹤參數。

</dd> <dt>

*szFormat* 
</dt> <dd>

描述追蹤格式的以零結尾的字串。

</dd> <dt>

*標記* 
</dt> <dd>

**Vsprintf** 函式的標記。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回 trace 語句的長度（以位元組為單位）。

## <a name="remarks"></a>備註

Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。

**Va \_ 清單** 資料類型是一種標準類型，可用來保存 **va \_ arg** 和 **va \_ end** 宏所需的資訊。 如需詳細資訊，請參閱 [標準類型](/cpp/c-runtime-library/standard-types?view=vs-2019)。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

