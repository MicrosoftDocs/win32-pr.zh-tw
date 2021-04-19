---
description: 設定離線登錄區中所指定登錄機碼值的資料。
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: 'ORSetValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978487"
---
# <a name="orsetvalue-function"></a>ORSetValue 函式

設定離線登錄區中所指定登錄機碼值的資料。

## <a name="syntax"></a>語法


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpValueName* \[在中，選擇性\]
</dt> <dd>

要設定的值名稱。 如果索引鍵中沒有這個名稱的值，則函式會將它新增至索引鍵。

如果 *lpValueName* 為 **Null** 或空字串 ""，則函式會設定索引鍵未命名或預設值的類型和資料。

如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。

登錄機碼沒有預設值，但可以有一個未命名的值，它可以是任何類型。

</dd> <dt>

*dwType* \[在\]
</dt> <dd>

*LpData* 參數所指向的資料類型。 如需可能類型的清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。

</dd> <dt>

*lpData* \[在中，選擇性\]
</dt> <dd>

要儲存的資料。

如果是以字串為基礎的類型，例如 REG \_ SZ，則字串必須以 null 結束。 若為 REG \_ 多重 \_ SZ 資料類型，字串必須以兩個 null 字元結束。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

*LpData* 參數所指向的資訊大小（以位元組為單位）。 如果資料的類型是 REG \_ SZ、reg \_ EXPAND \_ sz 或 REG \_ 多重 \_ SZ， *cbData* 必須包含終止的 null 字元或字元的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

## <a name="remarks"></a>備註

值大小會受到可用記憶體的限制。 Long 值 (超過2048個位元組) 應儲存為檔案，並將檔案名儲存在登錄中。 這有助於登錄有效率地執行。 應用程式元素（例如圖示、點陣圖和可執行檔）應該儲存為檔案，而不是放在登錄中。

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
