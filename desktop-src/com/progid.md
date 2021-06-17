---
title: ProgID
description: 瞭解 HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID 登錄機碼，這會將 ProgID 與 CLSID 相關聯。
ms.assetid: 89060943-7007-418b-a544-effbad548e87
keywords:
- ProgID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486f7e30bb0caff72eca3ad68191aaf50ab70280
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262720"
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

 

 




