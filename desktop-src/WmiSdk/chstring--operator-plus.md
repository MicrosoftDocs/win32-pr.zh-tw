---
description: + 串連運算子會聯結兩個字串，並傳回 CHString 物件。
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString：： operator + (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ce52e8740fcd420600aaebb192c23ab7269c4ddf14c068a4980c59df3e7773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097348"
---
# <a name="chstringoperator"></a>CHString：： operator +

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

+ 串連運算子會聯結兩個字串，並傳回 [**CHString**](chstring.md) 物件。

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str、str1、str2*
</dt> <dd>

串連的 [**CHString**](chstring.md)字串。

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*>ch*
</dt> <dd>

串連至字串或串連為字元之字串的字元。

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

以 **Null** 結束的字元字串指標。

</dd> </dl>

## <a name="return-values"></a>傳回值

此串連運算子會傳回 [**CHString**](chstring.md) 物件，該物件為串連的暫時結果。 這個傳回值可以在同一個運算式中合併數個串連。

## <a name="remarks"></a>備註

這兩個引數字串的其中一個必須是 [**CHString**](chstring.md) 物件;另一個可以是字元指標或字元。 請注意，當您使用串連運算子時，可能會發生記憶體例外狀況，因為可以配置新的儲存體來保存暫存資料。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 **CHString：： operator +**：


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
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

 

