---
description: 回呼函數，用來在捕捉或播放期間通知主機錯誤。
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFileIOCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1adc4fdc72cd26e317a2d8dc4a82049a2ef6ad99734d5e8bfc631bffdf4df99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981518"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback：： ResultCallback 方法

回呼函數，用來在捕捉或播放期間通知主機錯誤。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a>參數

*resultState*   
指出所遇到的錯誤類型。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IFileIOCallback**](/windows/desktop/direct3dtools/ifileiocallback)

 

 
