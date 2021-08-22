---
description: 列舉離線登錄區中指定之開啟登錄機碼的值。 函數會在每次呼叫函式時，取得指定索引鍵下某個值的資訊。
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: 'OREnumValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 57a65e8fd862215bd6281e487520857580cf6026b94b2ca375079f84407e4cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331798"
---
# <a name="orenumvalue-function"></a>OREnumValue 函式

列舉離線登錄區中指定之開啟登錄機碼的值。 函數會在每次呼叫函式時，取得指定索引鍵下某個值的資訊。

## <a name="syntax"></a>語法


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
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

要抓取之值的索引。 第一次呼叫函式時，此參數應為零，然後在後續呼叫中遞增。

因為值未排序，所以任何新的值都會有任意的索引。 這表示函數可能會以任何順序傳回值。

</dd> <dt>

*lpValueName* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會以 null 終止字串的形式接收值的名稱。 這個緩衝區必須夠大，才能包含終止的 null 字元。

如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。

</dd> <dt>

*lpcValueName* \[in、out\]
</dt> <dd>

變數的指標，該變數會指定 *lpValueName* 參數所指向的緩衝區大小（以字元為單位）。 當函式傳回時，變數會接收儲存在緩衝區中的字元數，而不包含終止的 null 字元。

</dd> <dt>

*lpType* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。 如需可能的類型代碼清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。 如果不需要類型程式碼，則 *lpType* 參數可以是 **Null** 。

</dd> <dt>

*lpData* \[out、optional\]
</dt> <dd>

接收值專案資料之緩衝區的指標。 如果資料不是必要的，則此參數可以是 **Null** 。

如果 *lpData* 為 **Null** ，而 *lpcbData* 為非 **Null**，則函式會將資料大小（以位元組為單位）儲存在 *lpcbData* 所指向的變數中。 這可讓應用程式判斷為數據配置緩衝區的最佳方式。

</dd> <dt>

*lpcbData* \[in、out、optional\]
</dt> <dd>

變數的指標，該變數會指定 *lpData* 參數所指向的緩衝區大小（以位元組為單位）。 當函式傳回時，變數會接收儲存在緩衝區中的位元組數目。

只有當 *lpData* 為 **null** 時，此參數才可以是 **null** 。

如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則此大小包含任何終止的 null 字元或字元。 如需詳細資訊，請參閱＜備註＞。

如果 *lpData* 所指定的緩衝區不夠大，無法容納資料，則函數會傳回錯誤 \_ \_ 的資料，並將所需的緩衝區大小儲存在 *lpcbData* 所指向的變數中。 在此情況下， *lpData* 的內容是未定義的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果 *lpData* 緩衝區太小而無法接收值，函數會傳回錯誤的 \_ \_ 資料。

## <a name="remarks"></a>備註

若要列舉值，應用程式一開始應該呼叫 **OREnumValue** 函數，並將 *dwIndex* 參數設定為零。 然後，應用程式應該遞增 *dwIndex* 並呼叫 **OREnumValue** 函式，直到不再有值 (為止，直到函式傳回錯誤 \_ \_) 沒有其他專案為止 \_ 。

應用程式也可以在第一次呼叫函式時，將 *dwIndex* 設定為最後一個值的索引，並遞減索引，直到列舉索引0的值為止。 若要取出最後一個值的索引，請使用 [**ORQueryInfoKey**](orqueryinfokey.md) 函數。

使用 **OREnumValue** 時，應用程式不應該呼叫可能會變更所查詢金鑰的任何離線登錄功能。

如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則字串可能未以正確的 null 終止字元儲存。 因此，即使函式傳回錯誤 \_ 成功，應用程式仍應確定字串在使用之前已正確地終止; 否則，它可能會覆寫緩衝區。  (請注意，REG \_ 多重 \_ SZ 字串應該要有兩個 null 終止字元。 ) 

若要判斷名稱和資料緩衝區的大小上限，請使用 [**ORQueryInfoKey**](orqueryinfokey.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
