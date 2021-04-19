---
description: 完成使用 sprintf 樣式追蹤的選擇性欄位來設定追蹤緩衝區。
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978664"
---
# <a name="setasynctraceparamsex-function"></a>SetAsyncTraceParamsEx 函式

完成使用 **sprintf** 樣式追蹤的選擇性欄位來設定追蹤緩衝區。

## <a name="syntax"></a>語法


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszModule* 
</dt> <dd>

與追蹤相關聯的模組名稱。

</dd> <dt>

*pszFile* 
</dt> <dd>

包含例外狀況的原始程式檔名稱。

</dd> <dt>

*行* 
</dt> <dd>

來源檔案中例外狀況的行號。

</dd> <dt>

*pszFunction* 
</dt> <dd>

例外狀況的函式名稱。

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

追蹤旗標常數，表示其中一種可用的追蹤類型。 這個參數可以是下列任何一個值。

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**嚴重 \_追蹤 \_ 遮罩** (0x00000001) 
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**錯誤 \_追蹤 \_ 遮罩** (0x00000002) 
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG \_追蹤 \_ 遮罩** (0x00000004) 
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**狀態 \_追蹤 \_ 遮罩** (0x00000008) 
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_追蹤 \_ 遮罩** (0x00000010) 
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**訊息 \_ (\_** 0x00000020) 的追蹤遮罩
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**全部 \_追蹤 \_ 遮罩** (0xffffffff) 
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則此函數會傳回 1;否則，它會傳回0。

## <a name="remarks"></a>備註

Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
