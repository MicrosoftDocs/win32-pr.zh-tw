---
description: 除了 (COM) 註冊的一般元件物件模型之外，還必須完成下列步驟，才能註冊圖示重迭處理常式。
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: 如何註冊圖示重迭處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0e62d95b224b131f03c2bd976ddf7c01d7cb3de7ad6995f21568dc7e990d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714908"
---
# <a name="how-to-register-icon-overlay-handlers"></a>如何註冊圖示重迭處理常式

除了 (COM) 註冊的一般元件物件模型之外，還必須完成下列步驟，才能註冊圖示重迭處理常式。

## <a name="instructions"></a>指示

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>步驟1：為此金鑰下的處理常式建立名為的子機碼

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>步驟2：將子機碼的預設值設定為物件之類別識別碼的字串形式 (CLSID) GUID

下列範例說明如何註冊名為 MyOverlay 的圖示重迭處理常式。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



