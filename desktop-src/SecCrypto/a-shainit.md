---
description: 起始資料流程的雜湊。
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: 'A_SHAInit 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986801"
---
# <a name="a_shainit-function"></a>SHAInit 函式 \_

起始資料流程的雜湊。

## <a name="syntax"></a>語法


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*內容* \[in、out\]
</dt> <dd>

SHA 內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函式與 SHAInit 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。 如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| 程式庫<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
