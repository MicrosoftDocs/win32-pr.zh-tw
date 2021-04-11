---
description: " (API) 的部分信任問題和 StylusInput 應用程式設計介面的總覽。"
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: StylusInput API 的部分信任考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193947"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>StylusInput API 的部分信任考慮

使用 *控制碼* 參數的 [**RealTimeStylus**](realtimestylus-class.md)需要 [system.security.permissions.uipermissionwindow>. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)和 [System.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)許可權，以及使用 *attachedControl* 參數的函式所需的許可權。

如需安全性和信任問題的詳細資訊，請參閱 [安全性與信任](security-and-trust.md)。

 

 
