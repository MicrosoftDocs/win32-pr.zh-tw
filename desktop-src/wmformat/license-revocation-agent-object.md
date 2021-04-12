---
title: 授權撤銷代理程式物件
description: 授權撤銷代理程式物件
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK、授權撤銷代理程式物件
- Advanced Systems Format (ASF) 、授權撤銷代理程式物件
- ASF (Advanced 系統格式) 、授權撤銷代理程式物件
- 物件、授權撤銷代理程式物件
- 授權撤銷，授權撤銷代理程式物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374390"
---
# <a name="license-revocation-agent-object"></a>授權撤銷代理程式物件

授權撤銷代理程式物件會管理授權撤銷的用戶端。 授權撤銷是授權伺服器可以從用戶端電腦上的授權存放區中移除授權的程式。 此程式牽涉到在用戶端應用程式和授權伺服器之間傳遞數個訊息。 在此物件上公開的方法會處理並產生這些訊息。

授權撤銷代理程式物件是由 [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) 函式所建立，該函式會將指標設定為 [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) 介面。 **IUnknown** 和 **IWMLicenseRevocationAgent** 是此物件唯一支援的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> </dl>

 

 




