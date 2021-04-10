---
title: MiscStatus
description: 指定如何建立和顯示物件。
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021676"
---
# <a name="miscstatus"></a>MiscStatus

指定如何建立和顯示物件。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>備註

如需詳細資訊，請參閱 [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) 列舉和 [**IOleObject：： GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)。

如果找不到對應至 >DVASPECT 的子機碼，則會使用 **MiscStatus** 的預設值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




