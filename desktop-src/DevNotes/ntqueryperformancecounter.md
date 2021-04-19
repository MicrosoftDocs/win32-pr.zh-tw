---
description: 傳回效能計數器的目前值，並選擇性地傳回效能計數器的頻率。
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977461"
---
# <a name="ntqueryperformancecounter-function"></a>NtQueryPerformanceCounter 函式

\[這項功能不受支援，因此不應該使用。 請改用 **QueryPerformanceCounter** 和 **QueryPerformanceFrequency** 函數。\]

傳回效能計數器的目前值，並選擇性地傳回效能計數器的頻率。

## <a name="syntax"></a>語法


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PerformanceCounter* \[擴展\]
</dt> <dd>

要接收目前效能計數器值的變數位址。

</dd> <dt>

*PerformanceFrequency* \[out、optional\]
</dt> <dd>

要接收效能計數器頻率之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回「 **NTSTATUS** 程式碼」 **狀態 \_ 成功**; 否則，它會傳回錯誤代碼，例如 **狀態 \_ 存取 \_ 違規**。

## <a name="remarks"></a>備註

沒有適用于 **NtQueryPerformanceCounter** 的標頭檔。 雖然您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至 Ntdll.dll，但您應該使用上述替代函數。

效能頻率是效能計數器的頻率（以赫茲為單位），特別是每秒的計數。 此值與實值相依。 如果實值沒有硬體可支援效能時間，則傳回的值為0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
