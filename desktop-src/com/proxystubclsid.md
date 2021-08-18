---
title: ProxyStubClsid
description: 在16位 proxy Dll 中地圖 IID 寫入 CLSID。
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- ProxyStubClsid 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129990"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

在16位 proxy Dll 中地圖 IID 寫入 CLSID。

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

 

 




