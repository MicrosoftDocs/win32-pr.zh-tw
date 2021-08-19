---
title: COM)  (介面
description: 選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- 介面登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048116"
---
# <a name="interface-com"></a>COM)  (介面

選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>備註

如果此清單中沒有介面名稱，此類別的實例永遠不會支援此介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面金鑰](interface-key.md)
</dt> </dl>

 

 




