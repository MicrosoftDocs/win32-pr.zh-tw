---
title: 動詞命令
description: 指定要為應用程式註冊的動詞。
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- 動詞登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef70e4a3f748b1f00a364f25755d60a3adfd9091cd2df3032e347f53f55519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047716"
---
# <a name="verb"></a>動詞命令

指定要為應用程式註冊的動詞。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>備註

每個動詞都是以「*名稱*」、「*功能表 \_ 旗* 標」、「*動詞 \_ 旗* 標」形式的 **REG \_ SZ** 值。 動詞必須是連續的編號。

此 *名稱* 描述 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) 函式呼叫如何附加動詞。 例如「&Play」。

*功能表 \_ 旗* 標值會指出動詞應該如何出現在功能表中。 除了 MF [](/windows/win32/api/winuser/nf-winuser-appendmenua) \_ BITMAP、MF \_ OWNERDRAW 和 MF 快顯視窗以外，支援 AppendMenu 支援的所有旗標 \_ 。

*動詞 \_ 旗* 標值描述動詞的屬性。 使用 [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)中的其中一個值，或0。

如需詳細資訊，請參閱 [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)、 [**IOleObject：:D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)和 [**IOleObject：： EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 