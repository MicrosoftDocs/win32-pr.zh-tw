---
description: 您可以測試專案之 Shell 屬性的 SFGAO 旗標值，以判斷是否應啟用或停用動詞。
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: 如何使用專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849188"
---
# <a name="how-to-use-item-attributes"></a>如何使用專案屬性

您可以測試專案之 Shell 屬性的 [**SFGAO**](sfgao.md) 旗標值，以判斷是否應啟用或停用動詞。

若要使用此屬性功能，請在動詞命令底下新增下列 **REG \_ DWORD** 值：

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

AttributeMask 值會指定要測試之遮罩的位值 [**SFGAO**](sfgao.md) 值。

### <a name="step-2"></a>步驟 2:

AttributeValue 值會指定所測試之位的 [**SFGAO**](sfgao.md) 值。

### <a name="step-3"></a>步驟 3：

ImpliedSelectionModel 為專案動詞指定零，或在背景快捷方式功能表上指定非零的動詞。

## <a name="remarks"></a>備註

在下列範例登錄專案中，AttributeMask 會設定為 [**SFGAO \_ READONLY**](sfgao.md) (0x40000) 。

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



