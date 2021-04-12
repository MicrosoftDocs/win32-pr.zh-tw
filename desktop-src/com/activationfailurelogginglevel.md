---
title: ActivationFailureLoggingLevel
description: 針對元件啟動和啟用的失敗要求，設定事件記錄檔專案的詳細資訊。
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- ActivationFailureLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372633"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

針對元件啟動和啟用的失敗要求，設定事件記錄檔專案的詳細資訊。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值 | 描述                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 使用任意記錄。 預設會記錄失敗，但用戶端可以 \_ 在 CoCreateInstanceEx 中指定 CLSCTX NO \_ \_ [****](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)，來覆寫此行為。 這是預設值。 |
| 1     | 無論用戶端指定什麼，一律記錄所有失敗。                                                                                                                                                      |
| 2     | 請勿記錄任何失敗，不論用戶端是否已指定。                                                                                                                                                       |



 

如果您需要應用程式來控制事件記錄，建議您將此值設為0，並在需要時撰寫用戶端程式代碼加以覆寫。 強烈建議您不要將值設定為2。 如果事件記錄已停用，則更難診斷問題。 對於電腦限制許可權失敗，其中 COM 沒有 CLSCTX 位，COM 會將0的值視為1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




