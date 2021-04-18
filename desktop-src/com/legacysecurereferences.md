---
title: LegacySecureReferences
description: 判斷是否針對未呼叫 CoInitializeSecurity 的應用程式保護 AddRef/發行調用的安全。
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- LegacySecureReferences 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968642"
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

 

 




