---
title: CallFailureLoggingLevel
description: 設定有關元件呼叫失敗的事件記錄檔專案詳細程度。
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- CallFailureLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839771"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

設定有關元件呼叫失敗的事件記錄檔專案詳細程度。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值 | 描述                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | 在 COM 伺服器進程中進行呼叫時，一律會記錄失敗。                           |
| 2     | 絕對不要在 COM 伺服器進程的呼叫期間記錄失敗。 這是預設值。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




