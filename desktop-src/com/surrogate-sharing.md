---
title: 代理共用
description: 如果 DLL 伺服器具有相符的安全性識別，且共用相同的 AppID 值，就會共用代理。
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e159fff59144773633cfbe35bb1486e9eeb1014d02e23e0c9b95bcd817bb53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678408"
---
# <a name="surrogate-sharing"></a>代理共用

如果 DLL 伺服器具有相符的安全性識別，且共用相同的 AppID 值，就會共用代理。

預設會將 DLL 伺服器載入至自己的代理進程。 若要將其他 DLL 伺服器載入至現有的代理，讓它支援一部以上的 DLL 伺服器，有兩個需求：

-   DLL 伺服器必須具有相同的 AppID 值。
-   DLL 伺服器的安全性內容必須相同。

如果要在不同的安全性身分識別下啟動兩個 DLL 伺服器，它們必須位於不同的代理中，不論其 Appid 是否相符。

以下是使用 Appid 管理代理共用的範例：

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

comp1.dll 和 comp2.dll 的 DLL 元件的兩個 Clsid 已設定為共用 AppID。 [AppID](appid-key.md)索引鍵會指定[DllSurrogate](dllsurrogate.md)值，以指定可在代理中載入 DLL 伺服器。 在此範例中， **DllSurrogate** 值為空字串，表示應該使用 DLL 代理的預設系統執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DLL 伺服器需求](dll-server-requirements.md)
</dt> <dt>

[註冊 DLL 伺服器以進行代理程式啟用](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




