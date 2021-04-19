---
description: 抓取離線登錄 hive 中指定之登錄值的類型和資料。
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: 'ORGetValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994713"
---
# <a name="orgetvalue-function"></a>ORGetValue 函式

抓取離線登錄 hive 中指定之登錄值的類型和資料。

## <a name="syntax"></a>語法


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpSubKey* \[在中，選擇性\]
</dt> <dd>

登錄機碼的名稱。 此索引鍵必須是 *控制碼* 參數所指定之金鑰的子機碼。 此參數可以是 **Null**。

索引鍵名稱不區分大小寫。

</dd> <dt>

*lpValue* \[在中，選擇性\]
</dt> <dd>

登錄值的名稱。 如果此參數為 **Null** 或空字串 ""，則函式會抓取索引鍵未命名或預設值（如果有的話）的類型和資料。 如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。

索引鍵不會自動具有未命名或預設值。 未命名的值可以是任何類型。

值名稱不區分大小寫。

</dd> <dt>

*pdwType* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。 如需可能的類型代碼清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。 如果不需要型別，這個參數可以是 **Null** 。

</dd> <dt>

*pvData* \[out、optional\]
</dt> <dd>

接收值資料之緩衝區的指標。 如果資料不是必要的，則此參數可以是 **Null** 。

如果資料是字串，此函式會檢查終止的 null 字元。 如果找不到，則如果緩衝區夠大而足以容納額外的字元，則會以 null 結束字元儲存字串。 否則，此函式會失敗並傳回錯誤 \_ \_ 的資料。

</dd> <dt>

*pcbData* \[in、out、optional\]
</dt> <dd>

變數的指標，該變數會指定 *pvData* 參數所指向的緩衝區大小（以位元組為單位）。 當函數傳回時，這個變數會包含複製到 *pvData* 的資料大小。

只有在 *pvData* 為 **Null** 時， *PcbData* 參數才可以是 **null** 。

如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則此大小包含任何終止的 null 字元或字元。 如需詳細資訊，請參閱＜備註＞。

如果 *pvData* 參數指定的緩衝區不夠大，無法容納資料，則函數會傳回錯誤 \_ \_ 的資料，並將所需的緩衝區大小儲存在 *pcbData* 所指向的變數中。 在此情況下， *pvData* 緩衝區的內容是未定義的。

如果 *pvData* 為 **Null**，而 *pcbData* 為非 **Null**，則函式會傳回錯誤 \_ SUCCESS，並將資料的大小（以位元組為單位）儲存在 *pcbData* 所指向的變數中。 這可讓應用程式判斷為值的資料配置緩衝區的最佳方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

## <a name="remarks"></a>備註

應用程式通常會呼叫 [**OREnumValue**](orenumvalue.md) 函式來判斷值名稱，然後呼叫 **ORGetValue** 函數來取得名稱的資料。

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
