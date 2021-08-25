---
description: 用來通知主機引擎進度的回呼函數。 這也可做為主機判斷引擎是否仍在執行中的方式。
title: IStatusCallback：： Status 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3b945f4fcae0561ab1c08c497e18fcd0afc36425a2e3f90a06fb312f603328bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844838"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback：： Status 方法

用來通知主機引擎進度的回呼函數。 這也可做為主機判斷引擎是否仍在執行中的方式。

## <a name="syntax"></a>語法


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>參數

*dwMillisecondsElapsed*   
自上次撥號狀態以來經過的時間（以毫秒為單位）。

*dwFramesCaptured*   
自上次撥號狀態以來已捕捉的框架數目。

*dwFramesElapsed*   
自上次撥號狀態以來經過的框架數目。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S_OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
