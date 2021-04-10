---
description: 從存放庫中刪除類別的現有實例。
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026377"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

**Pragma deleteinstance** 命令會從存放庫中刪除類別的現有實例。

以下說明此命令的語法：


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* 是 MOF 編譯器從目前的命名空間中刪除之實例的唯一識別碼。

*\[ 旗 \]* 標必須是下列其中一個引數。



| 旗標   | 描述                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| 失敗   | 如果該類別不存在於存放庫中，則會導致 MOF 編譯器以錯誤訊息結束。 |
| nofail | 即使類別不存在，也會使 MOF 編譯器繼續進行。                                |



 

## <a name="examples"></a>範例

下列範例顯示如何使用此命令。


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




