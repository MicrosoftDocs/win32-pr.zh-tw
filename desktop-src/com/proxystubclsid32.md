---
title: ProxyStubClsid32
description: 將 IID 對應至32位 proxy Dll 中的 CLSID。
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316555"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

將 IID 對應至32位 proxy Dll 中的 CLSID。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>備註

這是指定 IID CLSID 的 **REG \_ SZ** 值。

這是必要的專案，因為在16位和32位介面上，IID 對 CLSID 的對應可能會不同。 IID 對 CLSID 的對應取決於將介面 proxy 封裝成一組 proxy Dll 的方式。

如果您加入介面，您必須使用此專案將它們註冊 (32 位系統) ，讓 OLE 可以找到適當的遠端程式碼來建立進程間的通訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**介面**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 