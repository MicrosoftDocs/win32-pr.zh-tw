---
description: 列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。 函式會在每次呼叫時，捕獲一個子機碼的相關資訊。
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: 'OREnumKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990937"
---
# <a name="orenumkey-function"></a>OREnumKey 函式

列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。 函式會在每次呼叫時，捕獲一個子機碼的相關資訊。

## <a name="syntax"></a>語法


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*dwIndex* \[在\]
</dt> <dd>

要取出的子機碼索引。 第一次呼叫函式時，此參數應為零，然後在後續呼叫中遞增。

因為子機碼不會排序，所以任何新的子機碼都會有任意的索引。 這表示函數可能會以任何順序傳回子機碼。

</dd> <dt>

*lpName* \[擴展\]
</dt> <dd>

接收子機碼名稱之緩衝區的指標，包括結束的 null 字元。 此函式只會將子機碼名稱（而不是完整金鑰階層）複製到緩衝區。 如果函式失敗，則不會將任何資訊複製到這個緩衝區。

如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。

</dd> <dt>

*lpcName* \[in、out\]
</dt> <dd>

變數的指標，這個變數會指定 *lpName* 參數在 **WCHARs** 中指定的緩衝區大小。 此大小應包含終止的 null 字元。 如果函式成功， *lpcName* 所指向的變數會包含儲存在緩衝區中的字元數，而不包含終止的 null 字元。

</dd> <dt>

*lpClass* \[out、optional\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收列舉子機碼之以 null 結束的類別字串。 此參數可以是 **Null**。

</dd> <dt>

*lpcClass* \[in、out、optional\]
</dt> <dd>

變數的指標，這個變數會指定 *lpClass* 參數在 **WCHARs** 中指定的緩衝區大小。 大小應包含終止的 null 字元。 如果函式成功， *lpcClass* 會包含儲存在緩衝區中的字元數，不包括終止的 null 字元。 只有當 *lpClass* 為 **null** 時，此參數才可以是 **null** 。

</dd> <dt>

*lpftLastWriteTime* \[out、optional\]
</dt> <dd>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構的指標，此結構會接收上次寫入列舉子機碼的時間。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。 可能的錯誤代碼包括下列各項：

-   如果 *lpName* 緩衝區太小而無法接收索引鍵的名稱，函數會傳回錯誤的 \_ \_ 資料。
-   如果沒有其他可用的子機碼，此函式會傳回 \_ 沒有 \_ 其他專案的錯誤 \_ 。

## <a name="remarks"></a>備註

若要列舉子機碼，應用程式一開始應該呼叫 **OREnumKey** 函數，並將 *dwIndex* 參數設定為零。 然後，應用程式應該遞增 *dwIndex* 參數並呼叫 **OREnumKey** ，直到沒有其他子機碼 (表示函式會傳回錯誤 \_) 的 \_ \_ 專案。

應用程式也可以在第一次呼叫函式時，將 *dwIndex* 設定為最後一個子機碼的索引，並遞減索引，直到列舉索引0的子機碼為止。 若要取出最後一個子機碼的索引，請使用 [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) 函數。

當應用程式使用 **OREnumKey** 函式時，它不應該呼叫任何可能會變更所列舉之索引鍵的離線登錄功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
