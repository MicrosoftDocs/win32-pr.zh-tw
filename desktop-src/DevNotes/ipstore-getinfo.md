---
description: 傳回存放裝置提供者的資訊。
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'IPStore：： GetInfo 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986576"
---
# <a name="ipstoregetinfo-method"></a>IPStore：： GetInfo 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

傳回存放裝置提供者的資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppProperties* \[擴展\]
</dt> <dd>

**PPST \_ PROVIDERINFO** 結構的指標，其中包含儲存提供者的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。 值為 **PST \_ E \_ OK** 表示函式已成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
