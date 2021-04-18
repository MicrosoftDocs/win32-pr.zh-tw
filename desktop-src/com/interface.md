---
title: COM)  (介面
description: 選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- 介面登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965268"
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

 

 




