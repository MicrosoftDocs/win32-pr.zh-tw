---
title: ProxyStubClsid
description: 將 IID 對應至16位 proxy Dll 中的 CLSID。
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- ProxyStubClsid 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021853"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

將 IID 對應至16位 proxy Dll 中的 CLSID。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>備註

這是指定 IID CLSID 的 **REG \_ SZ** 值。

如果您加入介面，您必須使用此專案將它們註冊 (16 位系統) ，讓 OLE 可以找到適當的遠端程式碼來建立進程間的通訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**介面**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




