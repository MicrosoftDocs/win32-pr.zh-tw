---
description: DllGetVersion 函數會使用 CABINETDLLVERSIONINFO 結構來抓取 Cabinet.dll 的版本號碼。
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994237"
---
# <a name="dllgetversion-function"></a>DllGetVersion 函式

\[不再支援此函式，因此無法保證其行為。\]

**DllGetVersion** 函數會使用 [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)結構來抓取 Cabinet.dll 的版本號碼。

## <a name="syntax"></a>語法


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcdvi* 
</dt> <dd>

包含版本資訊之 [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
