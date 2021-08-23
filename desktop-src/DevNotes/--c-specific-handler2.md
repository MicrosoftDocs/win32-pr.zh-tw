---
description: 由編譯器呼叫以執行結構化例外狀況處理延伸模組。
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: '__C_specific_handler 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017826"
---
# <a name="__c_specific_handler-function"></a>\_\_C \_ 特定 \_ 處理常式函數

由編譯器呼叫以執行結構化例外狀況處理延伸模組。

\_每當設定 FLAGS UNW \_ 旗標 \_ EHANDLER 或 UNW \_ 旗標 \_ UHANDLER 時，就會在回溯資訊中出現語言特定處理常式的相對位址。 特定語言的處理常式會在搜尋例外狀況處理常式時呼叫，或做為回溯的一部分來呼叫。 如需詳細資訊，請參閱 [語言特定處理常式](/cpp/build/language-specific-handler)。

## <a name="syntax"></a>語法


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ExceptionRecord* \[在\]
</dt> <dd>

提供包含標準 Win64 定義之例外狀況記錄的指標。

</dd> <dt>

*EstablisherFrame* \[在\]
</dt> <dd>

此函式之固定堆疊配置的基底位址。

</dd> <dt>

*CoNtextRecord* \[in、out\]
</dt> <dd>

指向例外狀況引發時的例外狀況內容 (在例外狀況處理常式案例中) 或終止處理常式案例中 (目前的「回溯」內容) 。

</dd> <dt>

*DispatcherCoNtext* \[in、out\]
</dt> <dd>

指向此函數的發送器內容。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wdm</dt> </dl>        |
| 程式庫<br/> | <dl> <dt>Ntoskrnl.exe .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

