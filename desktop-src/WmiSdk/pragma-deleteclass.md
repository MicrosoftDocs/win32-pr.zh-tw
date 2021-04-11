---
description: 從存放庫中刪除現有的類別及其實例。
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852475"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

**Pragma deleteclass** 預處理器命令會從存放庫中刪除現有的類別及其實例。

以下說明語法：


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* 是 MOF 編譯器從目前的命名空間中刪除之類別的名稱。

*\[ 旗 \]* 標必須是下列其中一個引數。



| 旗標   | 描述                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| 失敗   | 如果該類別不存在於存放庫中，則會導致 MOF 編譯器以錯誤訊息結束。 |
| nofail | 即使類別不存在，也會使 MOF 編譯器繼續進行。                                |



 

## <a name="examples"></a>範例

下列範例顯示如何使用此命令。


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 




