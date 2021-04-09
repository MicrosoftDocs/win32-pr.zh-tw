---
title: /WX 參數
description: /WX 參數指示 MIDL 編譯器在指定警告層級上，將所有錯誤處理為錯誤。
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX 參數 MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841387"
---
# <a name="wx-switch"></a>/WX 參數

**/Wx** 參數指示 MIDL 編譯器在指定警告層級上，將所有錯誤處理為錯誤。

``` syntax
midl /WX
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

如果指定了 **/wx** 參數，且未指定 [**/w**](-w.md)*n* 參數，則預設層級1的所有警告都會視為錯誤。

[**/W**](-w.md)*n* 參數會指示編譯器顯示層級 *n* 的所有警告，而 **/wx** 則會指示編譯器將所有警告視為錯誤處理。 這兩個參數的組合會指示編譯器將層級 *n* 的所有警告視為錯誤處理。

錯誤與警告不同。 錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。 警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。

警告-層級零 (0) 指示 MIDL 編譯器隱藏警告資訊。 結合 **/W0** 和 **/wx** 參數時，MIDL 編譯器會隱藏所有警告資訊。 在此情況下， **/wx** 參數沒有任何作用。

## <a name="examples"></a>範例

**midl/WX 檔案名 .idl**

**midl/W3/WX 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




