---
title: ActivateAtStorage
description: 將用戶端設定為將相同電腦上的物件具現化，其為它們正在使用或從中初始化的持續性狀態。
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048896"
---
# <a name="activateatstorage"></a>ActivateAtStorage

將用戶端設定為將相同電腦上的物件具現化，其為它們正在使用或從中初始化的持續性狀態。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。 開頭為 ' Y ' 或 ' y ' 的任何值都表示應使用 **ActivateAtStorage** 。

**ActivateAtStorage** 功能提供透明的方式，讓用戶端能夠在與使用的資料相同的電腦上尋找執行中的物件。 這可減少網路流量，因為物件會執行本機檔案系統呼叫，而不是跨網路的呼叫。

當設定 **ActivateAtStorage** 的值時，這會成為呼叫 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) 和 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) 函式的預設行為，以及 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)的檔案標記實值。 在這些呼叫中，指定 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) 結構會覆寫函式呼叫期間的 **ActivateAtStorage** 設定。 呼叫端可以透過 [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)結構，將 **COSERVERINFO** 資訊傳遞至 **IMoniker：： BindToObject** 。

 \_ \_ 如果未在用戶端的電腦上安裝類別的登錄資訊，則在指定 CLSCTX 遠端伺服器時，ActivateAtStorage 設定的值也會是預設行為。 為了充分利用 **ActivateAtStorage** 而撰寫的用戶端應用程式，可能需要較少的系統管理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> </dl>

 

 