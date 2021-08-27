---
description: 回呼函式，用來通知主機與呼叫堆疊相關聯之來源檔案的相關資訊。
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a50dba592f67a4628501d6a9a92bfe379daed09
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626344"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback：： ResultCallback 方法

回呼函式，用來通知主機與呼叫堆疊相關聯之來源檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a>參數

*計數*   
傳回的原始程式檔數目。

*count0 \_ sourceFileInfoBuffer*   
來源檔案。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**ISourceFileInfoCallback**](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
