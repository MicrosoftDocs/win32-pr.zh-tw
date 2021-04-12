---
description: 包含可當地語系化之列印表單的相關資訊。
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: 'FORM_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192597"
---
# <a name="form_info_2-structure"></a>表單 \_ 資訊 \_ 2 結構

包含可當地語系化之列印表單的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

表單內容。 下列是已定義的值，但只能設定一個值。 當 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)傳回 **表單 \_ INFO \_ 2** 時，**旗標** 會設定為表單資料庫中目前的值。



| 值         | 意義                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 表單 \_ 使用者    | 如果設定此位旗標，使用者就會定義表單。 具有此旗標集合的表單是在登錄中定義。                                                                                                                                                                    |
| 表單內 \_ 建 | 如果設定此位旗標，則表單是多工緩衝處理器的一部分。 具有此旗標設定的表單定義不會出現在登錄中。 無法修改內建表單，因此當結構傳遞至 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時，不應設定此旗標。 |
| 表單 \_ 印表機 | 如果設定了這個位旗標，表單就會與特定的印表機相關聯，而且其定義會出現在登錄中。                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

指定表單名稱之以 null 結束的字串指標。 表單名稱不能超過31個字元。

</dd> <dt>

**大小**
</dt> <dd>

表單的寬度和高度（以毫米為單位）。

</dd> <dt>

**ImageableArea**
</dt> <dd>

印表機可以列印之頁面區域的寬度和高度（以千為單位）。

</dd> <dt>

**pKeyword**
</dt> <dd>

表單的不可當地語系化字串識別碼指標。 傳遞至 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時，這會提供呼叫端在所有地區設定中識別表單的方法。

</dd> <dt>

**StringType**
</dt> <dd>

指定如何在執行時間取得表單的當地語系化顯示名稱。 以下是定義的值。 在任何指定的 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)呼叫中只能設定一個。 您 \_ \_ 可以使用 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)所傳回的 **表單 \_ INFO \_ 2** (s) 來設定字串 MUIDLL 和字串 LANGPAIR。 請參閱＜備註＞。



| 值            | 意義                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 字串 \_ 無     | 沒有當地語系化的顯示名稱。                                                                                                                                                            |
| 字串 \_ MUIDLL   | 顯示名稱會從 **pMuiDll** 中指定的 [多語系消費者介面](/windows/desktop/Intl/mui-resource-management)當地語系化的資源 DLL 中解壓縮。 識別碼位於 **dwResourceId** 成員中。 |
| 字串 \_ LANGPAIR | 顯示名稱和語言識別項是由 **pDisplayName** 直接提供，而語言則是由 **wLangId** 所指定。                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

包含當地語系化顯示名稱的 [多語系消費者介面](/windows/desktop/Intl/mui-resource-management) 當地語系化資源 DLL。

</dd> <dt>

**dwResourceId**
</dt> <dd>

表單在 **pMuiDll** 中的顯示名稱的資源識別碼。

</dd> <dt>

**pDisplayName**
</dt> <dd>

表單的顯示名稱，以 **wLangId** 所指定的語言顯示。

</dd> <dt>

**wLangId**
</dt> <dd>

**PDisplayName** 的語言。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時：

-   如果 **StringType** 為 STRING \_ NONE，則 **pMuiDll** 和 **pDisplayName** 都必須是 **Null** ，而且 **dwResourceId** 和 **wLangId** 都必須是0。
-   如果 **StringType** 是字串 \_ MUIDLL，則 **pDisplayName** 必須是 **Null** ，而 **wLangId** 必須是0。
-   如果 **StringType** 是字串 \_ LANGPAIR，則 **pMuiDll** 必須是 **Null** ，而 **dwResourceId** 必須是0。

針對 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)的呼叫所傳回的 **表單 \_ 資訊 \_ 2** ：

-   如果 **StringType** 同時是字串 \_ MUIDLL 和字串 \_ LANGPAIR， **pMuiDll**、 **pDisplayName**、 **dwResourceId** 和 **wLangId** 都會有有效的值。
-   如果 **StringType** \_ 僅限字串 MUIDLL，則 **pMuiDll** 和 **dwResourceId** 將會有有效的值。 **pDisplayName** 會是 **Null** ，而 **wLangId** 將會是0。
-   如果 **StringType** \_ 僅限字串 LANGPAIR，則 **pDisplayName** 和 **wLangId** 將會有有效的值。 **pMuiDll** 會是 **Null** ，而 **dwResourceId** 將會是0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 表單 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 表單 \_ 資訊 \_ 2a** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[多語系使用者介面](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

