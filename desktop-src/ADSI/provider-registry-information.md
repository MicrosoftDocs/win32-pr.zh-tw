---
title: 提供者登錄資訊
description: 本主題說明新增 ADSI 提供者時需要設定的索引鍵和值。
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838864"
---
# <a name="provider-registry-information"></a>提供者登錄資訊

此提供者會使用下列索引鍵和值向 ADSI 註冊：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

此提供者會使用下列索引鍵和值向 Windows 註冊：

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

提供者命名空間會使用下列索引鍵和值向 Windows 註冊：

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

在先前的段落中， *提供* 者是提供者最上層物件的識別碼。 *提供者命名空間* 是物件的識別碼，該物件會實作為提供者的命名空間。

如需特定範例，請參閱 [安裝範例提供者元件](installing-the-example-provider-component.md)。

 

 




