---
description: 建立額外的列舉值，這個列舉值包含與目前相同的列舉狀態。
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: 'IEnumPStoreTypes：： Clone 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4ac088ae708b62f458d7bba52127dadc8ef77c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981395"
---
# <a name="ienumpstoretypesclone-method"></a>IEnumPStoreTypes：： Clone 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

建立額外的列舉值，這個列舉值包含與目前相同的列舉狀態。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppenum* \[擴展\]
</dt> <dd>

指向 [**IEnumPStoreItems**](ienumpstoreitems.md) 指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
