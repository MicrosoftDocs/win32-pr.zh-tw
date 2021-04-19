---
description: + = 串連運算子會將字元加入至這個字串的結尾。 運算子接受其他 CHString 物件、字元指標或單一字元。
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString：： operator + = (ChString .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977362"
---
# <a name="chstringoperator"></a>CHString：： operator + =

\[[**CHString**](chstring.md)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

+ = 串連運算子會將字元加入至這個字串的結尾。 運算子接受其他 [**CHString**](chstring.md) 物件、字元指標或單一字元。

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*字串*
</dt> <dd>

串連至此字串的 [**CHString**](chstring.md) 字串。

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*>ch*
</dt> <dd>

要串連至此字串的字元。

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

要串連至此字串之以 **Null** 結束的字串指標。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，當您使用此串連運算子時，可能會發生記憶體例外狀況，因為新的儲存空間可能會針對新增至這個 [**CHString**](chstring.md) 物件的字元配置。

## <a name="examples"></a>範例

下列範例示範如何使用 **CHString：： operator + =**：


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
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

 

