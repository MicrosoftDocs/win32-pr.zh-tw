---
description: 用於設定指定的參數資訊。
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'IPStore：： GetProvParam 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977598"
---
# <a name="ipstoregetprovparam-method"></a>IPStore：： GetProvParam 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

\[這個方法尚未實作。\]

用於設定指定的參數資訊。 但是請注意，它不會執行，而且一律會失敗。

## <a name="syntax"></a>語法


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwParam* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*pcbData* \[擴展\]
</dt> <dd>

保留的。

</dd> <dt>

*ppbData* \[擴展\]
</dt> <dd>

保留的。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

呼叫這個方法一律會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
