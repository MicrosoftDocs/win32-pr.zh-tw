---
description: CHString 指派 (=) 運算子會以新資料重新初始化現有的 CHString 物件。
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString：： operator = (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026856"
---
# <a name="chstringoperator"></a>CHString：： operator =

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

[**CHString**](chstring.md)指派 (=) 運算子會以新資料重新初始化現有的 CHString 物件。

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*、 *p*
</dt> <dd>

將 [**CHString**](chstring.md) 字串指派給這個物件。

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*>ch*
</dt> <dd>

將字元指派給這個物件。

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*、 *psz*
</dt> <dd>

將以 **Null** 終止的字串指派給這個物件。

</dd> </dl>

## <a name="remarks"></a>備註

如果目的地字串 (也就是，左邊的) 已經夠大，足以儲存新的資料，就不會執行任何新的記憶體配置。 不過，每當您使用指派運算子時，都可能會發生記憶體例外狀況，因為通常會配置新的儲存體來保存所產生的 [**CHString**](chstring.md) 物件。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 **CHString：： operator =**：


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>ChString (包含 FwCommon) </dt> </dl>                                                    |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

