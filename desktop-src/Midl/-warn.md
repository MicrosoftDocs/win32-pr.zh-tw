---
title: /warn 參數
description: /Warn 參數會指定 MIDL 編譯器的警告層級。
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn 參數 MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067450"
---
# <a name="warn-switch"></a>/warn 參數

**/Warn** 參數會指定 MIDL 編譯器的警告層級。

``` syntax
midl /warn level
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*level* 
</dt> <dd>

指定警告層級，此為0到4範圍內的整數。 **/Warn** 參數和表示警告層級值的數位之間沒有空格。

</dd> </dl>

## <a name="remarks"></a>備註

警告層級表示警告的嚴重性。 警告層級的範圍為1到4，值為零表示不顯示警告資訊。 最高嚴重性警告為層級1。 下表說明每個警告層級的警告。



| 警告層級 | 描述                                             | 範例                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | 沒有警告。                                            |                                                                           |
| 1             | 可能造成應用程式錯誤的嚴重警告。      | 未指定任何系結控制碼、未歸屬指標、衝突的參數。 |
| 2             | 可能會在使用者的操作環境中造成問題。 | 識別碼長度超過31個字元。 未指定預設聯集 arm。  |
| 3             | 保留的。                                               |                                                                           |
| 4             | 最低警告層級。                                   | 非 ANSI C 結構。                                                    |



 

警告與錯誤不同。 錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。 警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。

**/Warn** 參數所設定的警告層級可以與 [**WX**](-wx.md)參數搭配使用，以使 MIDL 編譯器停止處理 IDL 檔案。

**/Warn** 參數的行為與 [**/w**](-w.md)參數相同。

## <a name="examples"></a>範例

**midl/warn2 檔案名 .idl**

**midl/warn4 bar .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




