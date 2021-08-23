---
description: 找出指定之匯入的目標函式，並將匯入 Thunk 中的函式指標取代為函式實作為目標。
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571548"
---
# <a name="resolvedelayloadedapi-function"></a>ResolveDelayLoadedAPI 函式

找出指定之匯入的目標函式，並將匯入 Thunk 中的函式指標取代為函式實作為目標。

## <a name="syntax"></a>語法


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ParentModuleBase* \[在\]
</dt> <dd>

匯入延遲載入函數的模組基底位址。

</dd> <dt>

*DelayloadDescriptor* \[在\]
</dt> <dd>

要載入之模組的描述元。

</dd> <dt>

*FailureDllHook* \[在中，選擇性\]
</dt> <dd>

失敗攔截的位址。 請參閱 [**DelayLoadFailureHook**](delayloadfailurehook.md)。

</dd> <dt>

*FailureSystemHook* \[在中，選擇性\]
</dt> <dd>

系統失敗攔截的位址。

</dd> <dt>

*ThunkAddress* \[擴展\]
</dt> <dd>

目標函數的 Thunk 資料。 用來尋找函數的特定名稱資料表專案。

</dd> <dt>

*旗標* 
</dt> <dd>

保護必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

匯入的位址，或其失敗的存根。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Delay-Loaded Dll 的連結器支援](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




