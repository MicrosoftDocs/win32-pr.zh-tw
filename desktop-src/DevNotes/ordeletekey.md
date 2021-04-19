---
description: 從離線登錄 hive 刪除子機碼及其值。
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: 'ORDeleteKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984405"
---
# <a name="ordeletekey-function"></a>ORDeleteKey 函式

從離線登錄 hive 刪除子機碼及其值。

## <a name="syntax"></a>語法


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。 [**ORCreateKey**](orcreatekey.md)或 [**OROpenKey**](oropenkey.md)函數會傳回此控制碼。

</dd> <dt>

*lpSubKey* \[在中，選擇性\]
</dt> <dd>

要刪除之金鑰的名稱。 它必須是 *處理* 識別之金鑰的子機碼，但不能有子機碼。

如果子機碼不存在，則函式會傳回「找不到錯誤」 \_ \_ 。

如果這個參數為 **Null**，則函式會刪除 *Handle* 參數所指定的索引鍵。 如果 *Handle* 參數所指定的索引鍵是 hive 的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。

索引鍵名稱不區分大小寫。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。 可能的錯誤代碼包括下列各項：

-   如果指定的子機碼不存在，則函數會 \_ 傳回 \_ 找不到的錯誤檔案 \_ 。
-   如果指定的子機碼是登錄區的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。
-   如果指定的子機碼有子機碼，此函式會傳回錯誤索引 \_ 鍵的 \_ 子系 \_ 。

## <a name="remarks"></a>備註

如果指定的登錄機碼存在，則會標示為已刪除。 未移除已刪除的金鑰，直到其最後一個控制碼關閉為止。

要刪除的金鑰不能有子機碼。 若要刪除索引鍵及其所有子機碼，請使用 [**OREnumKey**](orenumkey.md) 函式來列舉子機碼，並個別將其刪除。

只有 [**ORCloseKey**](orclosekey.md) 函數可以在已刪除的金鑰上呼叫;所有其他離線登錄作業都會失敗。 如果已刪除的金鑰是藉由呼叫 [**ORCreateKey**](orcreatekey.md)來明確建立的，則會在最後一個已刪除金鑰的控制碼關閉時釋出與該金鑰相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
