---
description: 根據指定的旗標，控制建立或更新實例的方式。
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195058"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

**Pragma instanceflags** 預處理器命令會根據指定的旗標，控制建立或更新實例的方式。

以下說明語法：


```mof
#pragma instanceflags ([Flag])
```



*\[ 旗 \]* 標必須是下列其中一個引數。



| 旗標       | 描述                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| 以 | 防止編譯器變更 MOF 檔案中的任何現有實例。                                |
| updateonly | 防止編譯器在 MOF 檔案中指定的實例不存在時建立新的實例。 |



 

## <a name="examples"></a>範例

下列範例顯示如何使用此命令。


```mof
#pragma instanceflags("createonly")
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

 

 




