---
title: ProxyStubClsid32
description: 將 IID 地圖32位 proxy Dll 中的 CLSID。
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- ProxyStubClsid32 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309894"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

將 IID 地圖32位 proxy Dll 中的 CLSID。

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

 

 