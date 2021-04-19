---
description: 抓取目前進程之動態卸載模組清單的大小與位置。
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979455"
---
# <a name="rtlgetunloadeventtraceex-function"></a>RtlGetUnloadEventTraceEx 函式

抓取目前進程之動態卸載模組清單的大小與位置。

## <a name="syntax"></a>語法


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ElementSize* \[擴展\]
</dt> <dd>

變數的指標，其中包含清單中元素的大小。

</dd> <dt>

*ElementCount* \[擴展\]
</dt> <dd>

變數的指標，其中包含清單中的元素數目。

</dd> <dt>

*EventTrace* \[擴展\]
</dt> <dd>

**RTL 卸載 \_ \_ 事件 \_ 追蹤** 結構的陣列指標。 如需詳細資訊，請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

載入器會將卸載的事件資訊儲存在可跨進程讀取的位置，方法是利用在所有進程的相同基底位址載入 Ntdll.dll 的事實。 當偵錯工具需要查詢卸載的模組資訊時，它會呼叫此函式來判斷變數所在的位址，然後在這些位址上查詢目標進程中的虛擬記憶體，以讀取實際值。

清單中的每個元素都定義如下。

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

此函數沒有相關聯的標頭檔。 相關聯的匯入程式庫（Ntdll.dll）可在 Windows 驅動程式套件 (WDK) 中取得。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數呼叫這個函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
