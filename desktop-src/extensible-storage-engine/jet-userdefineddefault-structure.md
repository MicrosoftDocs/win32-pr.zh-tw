---
description: 深入瞭解： JET_USERDEFINEDDEFAULT 結構
title: JET_USERDEFINEDDEFAULT 結構
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000183"
---
# <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT 結構

**JET_USERDEFINEDDEFAULT** 結構會與 JET_bitColumnUserDefinedDefault 一起指定，以提供新的資料行使用回呼決定的預設值。 這項技術可以用來執行計算的資料行。

**WINDOWS XP：** 在 Windows XP 中引進 **JET_USERDEFINEDDEFAULT** 結構。

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>成員

**szCallback**

以 "module function" 格式執行回呼的函式的匯出名稱 \! 。

回呼會保存為數據行架構的一部分。 函數的實際主機可執行檔和匯出名稱必須保存，才能在執行時間查閱函數的真真實位址。

模組名稱是包含函數的主機二進位檔名稱。 函數名稱是該函式的匯出名稱。 資料庫引擎會在執行時間使用這兩項資訊來找出回呼的真正位址，方法是對模組名稱執行 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 呼叫，然後在函式名稱後面加上 [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 呼叫。

例如，如果回呼是在稱為 MyCallback.DLL 的 DLL 中執行，而且該 DLL 儲存在 C： MyApplication 中，而且實回檔的函式 \\ 從 DLL 匯出為 UserDefinedDefaultCallback，則所需的字串會是 "C： \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback"。

**注意**  Embedded " \! " 不支援回呼名稱的模組部分中的字元。

強烈建議您使用不是主機架構功能的回呼名稱。 例如，請勿使用裝飾為 stdcall () 的匯出， UserDefinedDefaultCallback@32 因為只有 x86 電腦才支援此呼叫慣例。 如果使用這類回呼，則資料庫只能在 x86 電腦上使用。 在此情況下，您應該使用別名來建立平臺中立的匯出。

強烈建議您使用正在執行回呼的模組名稱的完整路徑。 如果使用相對路徑，則裝載資料庫的進程可能會受到惡意二進位檔的攻擊。

應用程式應該只傳遞受信任的回呼給 database engine。 資料庫引擎會載入二進位檔，以在建立相關聯的資料行時驗證它是否存在。 如果二進位檔的路徑未經過驗證或知道被信任，則可能會攻擊裝載資料庫的進程。

**pbUserData**

當叫用時，要傳遞至回呼的使用者定義資料的獨立區塊。提供的資料區塊將會保存為數據行架構的一部分。 如此一來，資料區塊必須完全獨立，而且無法參考資料庫範圍以外的任何資料。

如果 **pbUserData** 為零，則會忽略 **cbUserData** 的值。 在此情況下，當叫用時，不會將使用者定義資料傳遞至回呼。

**cbUserData**

請參閱 **pbUserData**。

**szDependantColumns**

保留供未來使用。

這個成員應該一律設定為 Null。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) 和 <strong>JET_</strong> USERDEFINEDDEFAULT_A (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
