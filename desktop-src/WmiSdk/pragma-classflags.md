---
description: 根據指定的旗標，控制 WMI 建立或更新類別的方式。
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996626"
---
# <a name="pragma-classflags"></a>pragma classflags

**Pragma classflags** 預處理器命令會根據指定的旗標，控制 WMI 建立或更新類別的方式。

以下說明此命令的語法：


```mof
#pragma classflags ("[flag1], [flag2]")
```



*\[ 旗 \]* 標必須是下列一個或多個引數。 您可以結合彼此不互相矛盾的旗標。



| 旗標        | 描述                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 以  | 指示編譯器不要對現有的類別進行任何變更，而且如果在 MOF 檔案中指定的類別已經存在於 WMI 中，就會終止編譯。                                                                                                                                                                                                        |
| forceupdate | 存在衝突的子類別時，強制更新類別。 例如，如果您在子類別中定義類別辨識符號，而基類嘗試加入相同的辨識符號，使用此旗標會在子類別中刪除衝突的辨識符號，以使編譯器解決此衝突。 如果子類別有實例，則更新會失敗。 |
| safeupdate  | 即使子類別存在，也允許編譯器更新類別（如果變更不會造成與子類別的衝突）。 例如，這個旗標可讓您將新的屬性新增至基類，而不需要將屬性新增至任何既有的子類別。 如果子類別具有實例，則更新會失敗。                           |
| updateonly  | 指示編譯器不要建立任何新的類別，而且如果 MOF 檔案中指定的類別不存在，編譯器就會終止編譯。                                                                                                                                                                                                  |



 

## <a name="examples"></a>範例

下列範例示範如何使用此命令搭配 updateonly 和 forceupdate 旗標。


```mof
#pragma classflags ("updateonly", "forceupdate")
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

 

 




