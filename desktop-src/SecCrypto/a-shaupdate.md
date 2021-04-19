---
description: 將資料加入至指定的雜湊物件。
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: 'A_SHAUpdate 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995913"
---
# <a name="a_shaupdate-function"></a>SHAUpdate 函式 \_

將資料加入至指定的雜湊物件。

## <a name="syntax"></a>語法


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*內容* \[in、out\]
</dt> <dd>

SHA 內容。

</dd> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

雜湊表。

</dd> <dt>

*BufferSize* 
</dt> <dd>

緩衝區的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

您可以多次呼叫此函數，以計算長資料流程或不連續資料流程的雜湊。 在抓取雜湊值之前，必須先呼叫 [**\_ SHAFinal**](a-shafinal.md) 函數。

此函式與 SHAUpdate 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。 如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| 程式庫<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
