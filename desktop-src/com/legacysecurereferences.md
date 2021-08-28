---
title: LegacySecureReferences
description: 判斷是否針對未呼叫 CoInitializeSecurity 的應用程式保護 AddRef/發行調用的安全。
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- LegacySecureReferences 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736545"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

判斷是否 / 針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式保護 AddRef **發行** 調用。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。 值為 ' Y ' 或 ' y ' 表示 **AddRef** 和 **發行** 是安全的。 如果此登錄值不存在或設定為 ' Y ' 或 ' y ' 以外的值，則不會保護 **AddRef** 和 **發行** 。 啟用安全參考會減緩遠端呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> </dl>

 

 




