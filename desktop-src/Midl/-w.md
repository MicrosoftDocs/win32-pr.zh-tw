---
title: /W 參數
description: /W 參數指定 MIDL 編譯器的警告層級。 警告層級表示警告的嚴重性。
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W 參數 MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969083"
---
# <a name="w-switch"></a>/W 參數

**/W** 參數指定 MIDL 編譯器的警告層級。 警告層級表示警告的嚴重性。

``` syntax
midl /W level
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*level* 
</dt> <dd>

指定警告層級，此為0到4範圍內的整數。 **/W** 參數和表示警告層級值的數位之間沒有空格。

</dd> </dl>

## <a name="remarks"></a>備註

警告層級的範圍為1到4，值為零表示不顯示警告資訊。 最高嚴重性的警告為層級1。 下表說明每個警告層級的警告。



| 警告層級 | 描述                                             | 範例                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | 沒有警告。                                            |                                                                           |
| W1            | 可能造成應用程式錯誤的嚴重警告。      | 未指定任何系結控制碼、未歸屬指標、衝突的參數。 |
| W2            | 可能會在使用者的操作環境中造成問題。 | 識別碼長度超過31個字元。 未指定預設聯集 arm。  |
| W3            | 保留的。                                               |                                                                           |
| W4            | 最低警告層級。                                   | 非 ANSI C 結構。                                                    |



 

警告與錯誤不同。 錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。 警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。

**/W** 參數所設定的警告層級可以搭配 [**/wx**](-wx.md)參數使用，使 MIDL 編譯器停止處理 IDL 檔案。

**/W** 參數的行為與 [**/warn**](-warn.md)參數相同。

## <a name="examples"></a>範例

**midl/W2 檔案名 .idl**

**midl/W4 bar .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/warn**](-warn.md)
</dt> </dl>

 

 




