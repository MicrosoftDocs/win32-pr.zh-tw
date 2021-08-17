---
UID: ''
title: CaptureStackBackTrace 函式
description: 藉由向上查看堆疊來捕捉堆疊回溯追蹤。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279499"
---
# <a name="capturestackbacktrace-function"></a>CaptureStackBackTrace 函式

## <a name="description"></a>Description

藉由向上查看堆疊並記錄每個畫面格的資訊，來捕獲堆疊回溯追蹤。

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>參數

### <a name="framestoskip-in"></a>FramesToSkip [in]

從回溯追蹤的開頭跳過的框架數。

### <a name="framestocapture-in"></a>FramesToCapture [in]

要捕捉的框架數目。
您可以捕獲最多 **MAXUSHORT** 的畫面格。

**Windows Server 2003 和 Windows XP：** *FramesToSkip* 和 *FramesToCapture* 參數的總和必須小於63。

### <a name="backtrace-out"></a>BackTrace [out]

從目前堆疊追蹤所捕捉的指標陣列。

### <a name="backtracehash-out-optional"></a>BackTraceHash [out，optional]

可以用來組織雜湊資料表的值。
如果此參數為 **Null**，則不會計算任何雜湊值。

此值的計算方式是根據 BackTrace 陣列中傳回的指標值。
兩個相同的堆疊追蹤將會產生相同的雜湊值。

## <a name="returns"></a>傳回

已捕獲的框架數目。

## <a name="remarks"></a>備註

**CaptureStackBackTrace** 函式定義為 **RtlCaptureStackBackTrace** 函式 (定義包含在 Windows SDK 從 Windows Vista) 開始。
如需詳細資訊，請參閱 WinBase .h 和 WinNT. h。

## <a name="see-also"></a>另請參閱
