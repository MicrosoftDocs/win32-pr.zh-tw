---
description: 這些注標運算子會設定或取得指定索引處的元素。 這些運算子可方便替代 SetAt 和 GetAt 方法。
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray：： operator [] (ChStrArr .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987337"
---
# <a name="chstringarrayoperator--"></a>CHStringArray：： operator \[\]

\[[**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

這些注標運算子會設定或取得指定索引處的元素。 這些運算子可方便替代 [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) 和 [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) 方法。

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*
</dt> <dd>

大於或等於零且小於或等於 System.array.getupperbound 所傳回值的整數索引。 [ ](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>傳回值

注標運算子會傳回目前位於此索引的 [**CHString**](chstring.md) 指標元素。

## <a name="remarks"></a>備註

您可以使用第一個運算子來呼叫不是 **const** 的陣列、右邊的 (r-值) 或左邊 (左值) 指派語句的側邊。 第二個（呼叫 **const** 陣列）只能用在右邊。

如果在指派) 語句的左側或右側 (的注標是否超出範圍，就會判斷提示程式庫的偵錯工具版本。

## <a name="examples"></a>範例

下列程式碼範例示範如何使用 [**CHStringArray：： operator \[ \]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85))。


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>ChStrArr (包含 FwCommon) </dt> </dl>                                                    |
| 程式庫<br/>                  | <dl> <dt>FrameDyn .lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CHStringArray：： Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray：： GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray：： SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

