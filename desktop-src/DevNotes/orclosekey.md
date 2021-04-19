---
description: 關閉離線登錄 hive 中指定之登錄機碼的控制碼。
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: 'ORCloseKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993621"
---
# <a name="orclosekey-function"></a>ORCloseKey 函式

關閉離線登錄 hive 中指定之登錄機碼的控制碼。

## <a name="syntax"></a>語法


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果指定的索引鍵是登錄區的根機碼，此函式會失敗，並出現錯誤 \_ 不正確 \_ 參數。

## <a name="remarks"></a>備註

指定之索引鍵的控制碼在關閉後不應使用，因為它將不再有效。 金鑰控制碼不應超過所需的時間保持開啟。

使用 [**ORCloseHive**](orclosehive.md) 函式來關閉離線登錄 hive。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
