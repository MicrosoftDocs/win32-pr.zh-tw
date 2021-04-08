---
title: AuxUserType
description: 指定應用程式的簡短顯示名稱和應用程式名稱。
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670888"
---
# <a name="auxusertype"></a>AuxUserType

指定應用程式的簡短顯示名稱和應用程式名稱。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>備註

建議的 *ShortDisplayName* 長度上限為15個字元。 這個名稱會在功能表中使用，包括快顯功能表。

*ApplicationName* 應該包含應用程式的實際名稱 (例如「Acme Draw 2.0」 ) 。 這個名稱會用於 [**貼上特殊**] 對話方塊的 [**結果**] 欄位中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




