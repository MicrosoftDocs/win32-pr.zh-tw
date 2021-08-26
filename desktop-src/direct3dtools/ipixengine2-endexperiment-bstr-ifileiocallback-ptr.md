---
description: 結束 experiement 並完成圖形記錄檔。
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2：： EndExperiment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 87d49b1960d43d1d9e2b931b01c89e09ee3cb579
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623474"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2：： EndExperiment 方法

結束 experiement 並完成圖形記錄檔。

## <a name="syntax"></a>語法


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a>參數

*記錄檔*   
COM 字串，包含圖形記錄檔的名稱。

*pCallback*   
回呼的位址，用來指出 experiement 已結束。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
