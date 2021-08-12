---
title: 64位 Windows 中的遠端登入存取
description: 登錄重新導向程式可透過 RegConnectRegistry 函式，在64位 Windows 上提供登錄的遠端存取。
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- 遠端登入存取 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561449"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>64位 Windows 中的遠端登入存取

登錄重新導向程式可透過 [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)函式，在64位 Windows 上提供登錄的遠端存取。

如果用戶端是32位的應用程式，它會存取伺服器的預設32位登錄視圖。 如果用戶端是64位的應用程式，它會存取64位登錄視圖。

**Windows Server 2003：** 除非應用程式使用金鑰 \_ WOW64 32KEY 旗標，否則所有用戶端都會存取64位登錄視圖 \_ 。 當用戶端和伺服器都執行這些版本的 Professional 時，此行為會隨 Windows Server 2003 Service Pack 1 (SP1) 和 Windows XP Windows x64 Edition 變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄重新導向程式](registry-redirector.md)
</dt> <dt>

[登錄反映](registry-reflection.md)
</dt> </dl>

 

 