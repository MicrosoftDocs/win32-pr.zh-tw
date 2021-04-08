---
title: ProgID
description: 將 ProgID 與 CLSID 產生關聯。
ms.assetid: 89060943-7007-418b-a544-effbad548e87
keywords:
- ProgID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feec17db2cf16425968c64ef25759f284341bdb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673099"
---
# <a name="progid"></a>ProgID

將 ProgID 與 CLSID 產生關聯。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ProgID = value
```

## <a name="remarks"></a>備註

每個可以插入的物件類別都有一個 ProgID。 如需建立 ProgID 的詳細資訊，請參閱[ <ProgID> 金鑰](-progid--key.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[<ProgID> 關鍵](-progid--key.md)
</dt> <dt>

[**VersionIndependentProgID**](versionindependentprogid.md)
</dt> </dl>

 

 




