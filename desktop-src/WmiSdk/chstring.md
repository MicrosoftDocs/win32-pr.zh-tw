---
description: 下表列出 CHString 方法。
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: 'CHString 類別 (ChString) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979991"
---
# <a name="chstring-class"></a>CHString 類別

\[**CHString** 類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

下表列出 **CHString** 方法。

## <a name="members"></a>成員

**CHString** 類別具有下列類型的成員：

-   [建構函式](#constructors)
-   [方法](#methods)
-   [運算子](#operators)

### <a name="constructors"></a>建構函式

**CHString** 類別具有這些函式。



| 建構函式                           | 描述                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | 以各種方式來結構 **CHString** 字串。<br/> |



 

### <a name="methods"></a>方法

**CHString** 類別有這些方法。



| 方法                                                    | 描述                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | 從 **CHString** 資料配置 BSTR。<br/>                                                            |
| [**整理**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | 比較兩個字串 (區分大小寫;使用地區設定特有的資訊) 。<br/>                            |
| [**比較**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | 比較兩個字串 (區分大小寫的) 。<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | 比較兩個字串 (不區分大小寫) 。<br/>                                                            |
| [**空白**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | 強制字串具有 0 (零) 長度。<br/>                                                            |
| [**Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | 多載。 在較大的字串中尋找字元或子字串。<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | 從集合中尋找第一個相符的字元。<br/>                                                      |
| [**格式**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | 多載。 將字串格式化為 **sprintf** 。<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | 多載。 格式化訊息字串。<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | 將字串格式化為 **vsprintf** 。<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | 釋放先前配置給字串的任何額外記憶體，移除此字串的任何額外負荷。<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | 傳回字串緩衝區的大小。<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | 多載。 傳回指定位置的字元。<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | 傳回 **CHString** 字串中的字元指標。<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | 傳回 **CHString** 字串中的字元指標，並截斷為指定的長度。<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | 傳回 **CHString** 字串中資料的指標。<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | 傳回 **CHString** 字串中的 Unicode 字元數。<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | 測試 **CHString** 字串是否不包含任何字元。<br/>                                         |
| [**離開**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | 將字串的左邊部分（如 Basic **left $** 函數) ）解壓縮 (。<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | 從資源檔載入現有的 **CHString** 字串。<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | 停用參考計數，並保護緩衝區中的字串。<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | 將此字串中的所有字元轉換成小寫字元。<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | 反轉這個字串中的字元。<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | 將此字串中的所有字元轉換成大寫字元。<br/>                              |
| [**中級**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | 多載。 將字串的中間部分解壓縮 (例如) 的基本 **$** 函數。<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | 釋放 [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)所傳回之緩衝區的控制權。<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | 尋找較大字串內的字元;從結尾開始。<br/>                                      |
| [**對**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | 將字串的右邊部分 (如 Basic **right $** 函數) 。<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | 設定指定位置的字元。<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | 解壓縮只包含不在集合中之字元的子字串。<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | 解壓縮只包含集合中之字元的子字串。<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | 修剪字串中的前置空白字元。<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | 修剪字串中的尾端空白字元。<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | 啟用參考計數，並釋放緩衝區中的字串。<br/>                                   |



 

### <a name="operators"></a>運算子
`
The **CHString** class has these operators.`



| 運算子                                                                                            | 描述                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**operator！ = (CHString，CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | 比較兩個 **CHStrings** 是否不相等。<br/>                                                             |
| [**operator！ = (CHString，LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | 比較 **CHString** 與 **LPCWSTR** 是否不相等。<br/>                                             |
| [**運算元 \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | 傳回 [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))的指定位置運算子替代字元。<br/> |
| [**運算子 +**](chstring--operator-plus.md)                                                       | 串連兩個字串，並傳回新的字串。<br/>                                                     |
| [**運算子 + =**](chstring--operator-plus-equal.md)                                                | 將新字串串連至現有字串的結尾。<br/>                                            |
| [**operator < (CHString、LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | 比較 **CHString** 與 **LPCWSTR**。<br/>                                                            |
| [**operator < (CHString、CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | 比較兩個 **CHStrings**。<br/>                                                                            |
| [**operator <= (CHString，CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | 比較兩個 **CHStrings**。<br/>                                                                            |
| [**operator <= (CHString，LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | 比較 **CHString** 與 **LPCWSTR**。<br/>                                                            |
| [**運算子 =**](chstring--operator-equal.md)                                                      | 將新值指派給 **CHString** 字串。<br/>                                                          |
| [**operator = = (CHString，CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | 比較兩個 **CHStrings** 是否相等。<br/>                                                               |
| [**operator = = (CHString，LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | 比較 **CHString** 與 **LPCWSTR** 是否相等。<br/>                                               |
| [**operator > (CHString、CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | 比較兩個 **CHStrings**。<br/>                                                                            |
| [**operator > (CHString、LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | 比較 **CHString** 與 **LPCWSTR**。<br/>                                                            |
| [**operator >= (CHString，CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | 比較兩個 **CHStrings**。<br/>                                                                            |
| [**operator >= (CHString，LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | 比較 **CHString** 與 **LPCWSTR**。<br/>                                                            |
| [**運算子 LPCWSTR**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | 直接存取儲存在 **CHString** 字串中的字元做為 C 樣式字串。<br/>                      |



 

## <a name="remarks"></a>備註

類別的函式是 **CHString：： ~ CHString**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>ChString (包含 FwCommon) </dt> </dl>                                                    |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



