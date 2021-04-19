---
description: 抓取離線登錄 hive 中指定之登錄機碼的相關資訊。
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: 'ORQueryInfoKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996211"
---
# <a name="orqueryinfokey-function"></a>ORQueryInfoKey 函式

抓取離線登錄 hive 中指定之登錄機碼的相關資訊。

## <a name="syntax"></a>語法


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpClass* \[out、optional\]
</dt> <dd>

接收索引鍵類別的緩衝區指標。 此參數可以是 **Null**。

</dd> <dt>

*lpcClass* \[in、out、optional\]
</dt> <dd>

變數的指標，該變數會指定 *lpClass* 參數所指向的緩衝區大小（以字元為單位）。

大小應包含終止的 null 字元。 當函式傳回時，這個變數會包含儲存在緩衝區中之類別字串的大小。 傳回的計數不包含終止的 null 字元。 如果緩衝區不夠大，則函式會傳回錯誤 \_ \_ 的資料，而變數會包含字串的大小（以字元為單位），而不會計算終止的 null 字元。

如果 *lpClass* 為 **null**，則 *lpcClass* 可以是 **null**。

如果 *lpClass* 參數是有效的位址，但不 (*lpcClass* 參數，例如，如果 *lpcClass* 參數為 **Null**) 則函式會傳回錯誤 \_ 不正確 \_ 參數。

</dd> <dt>

*lpcSubKeys* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收指定之索引鍵所包含的子機碼數目。 此參數可以是 **Null**。

</dd> <dt>

*lpcMaxSubKeyLen* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收具有最長名稱的索引鍵子機碼大小（以 Unicode 字元為單位），不包含終止的 null 字元。 此參數可以是 **Null**。

</dd> <dt>

*lpcMaxClassLen* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收指定子機碼類別之最長字串的大小（以 Unicode 字元表示）。 傳回的計數不包含終止的 null 字元。 此參數可以是 **Null**。

</dd> <dt>

*lpcValues* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收與索引鍵相關聯的值數目。 此參數可以是 **Null**。

</dd> <dt>

*lpcMaxValueNameLen* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收索引鍵的最大值名稱大小（以 Unicode 字元為單位）。 大小不包含終止的 null 字元。 此參數可以是 **Null**。

</dd> <dt>

*lpcMaxValueLen* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收索引鍵值之間最長的資料元件大小（以位元組為單位）。 此參數可以是 **Null**。

</dd> <dt>

*lpcbSecurityDescriptor* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收金鑰安全描述項的大小（以位元組為單位）。 此參數可以是 **Null**。

</dd> <dt>

*lpftLastWriteTime* \[out、optional\]
</dt> <dd>

接收最後寫入時間的 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構指標。 此參數可以是 **Null**。

函數會設定 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構的成員，以表示上次修改索引鍵或其任何值專案的時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果 *lpClass* 緩衝區太小而無法接收類別的名稱，函數會傳回錯誤的 \_ \_ 資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> </dl>

 

 
