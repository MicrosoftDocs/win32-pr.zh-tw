---
description: 計算 MD5Update 函數所輸入之資料的最終雜湊。
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: 'A_SHAFinal 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994574"
---
# <a name="a_shafinal-function"></a>SHAFinal 函式 \_

計算 MD5Update 函數所輸入之資料的最終雜湊。

## <a name="syntax"></a>語法


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*內容* \[in、out\]
</dt> <dd>

SHA 內容。

</dd> <dt>

*結果* \[擴展\]
</dt> <dd>

產生的雜湊表。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函式與 SHAFinal 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。 如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| 程式庫<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
