---
description: GetMacAddressFromBlob 函式會從 BLOB 取出命名的 MAC 位址。
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: 'GetMacAddressFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001431"
---
# <a name="getmacaddressfromblob-function"></a>GetMacAddressFromBlob 函式

**GetMacAddressFromBlob** 函式會從 BLOB 取出命名的 MAC 位址。

## <a name="syntax"></a>語法


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pOwnerName* \[在\]
</dt> <dd>

BLOB 擁有者名稱的指標。

</dd> <dt>

*pCategoryName* \[在\]
</dt> <dd>

BLOB 類別目錄名稱的指標。

</dd> <dt>

*pTagName* \[在\]
</dt> <dd>

BLOB 標記名稱的指標。

</dd> <dt>

*pMacAddress* \[擴展\]
</dt> <dd>

BLOB 的 MAC 位址指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為描述錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




