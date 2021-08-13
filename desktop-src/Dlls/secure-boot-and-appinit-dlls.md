---
description: 從 Windows 8 開始， \_ 啟用安全開機時，會停用 AppInit dll 基礎結構。
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit Dll 和安全開機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256018"
---
# <a name="appinit-dlls-and-secure-boot"></a>AppInit Dll 和安全開機

從 Windows 8 開始， \_ 啟用安全開機時，會停用 AppInit dll 基礎結構。

## <a name="about-appinit_dlls"></a>關於 AppInit \_ dll

AppInit \_ dll 基礎結構可讓您輕鬆地攔截系統 api，方法是允許將自訂 dll 載入至每個互動式應用程式的位址空間中。 應用程式和惡意軟體都使用 AppInit Dll 的原因，是為了攔截 Api;載入自訂 DLL 之後，它可以攔截已知的系統 API 並執行替代功能。 只有一小部分的新式合法應用程式會使用這項機制來載入 Dll，而一組大型惡意程式碼會使用這項機制來危害系統。 即使合法的 AppInit \_ dll 也可能會不慎造成系統鎖死和效能問題，因此 \_ 不建議使用 AppInit dll。

## <a name="appinit_dlls-and-secure-boot"></a>AppInit \_ dll 和安全開機

Windows 8 採用 UEFI 和安全開機來改善整體系統完整性，並為複雜的威脅提供強式保護。 啟用安全開機時， \_ 會停用 AppInit dll 機制，以保護客戶免于惡意程式碼和威脅的侵害。

請注意，安全開機是 UEFI 通訊協定，而不是 Windows 8 功能。 如需 UEFI 和安全開機通訊協定規格的詳細資訊，請參閱 [https://www.uefi.org](https://www.uefi.org/) 。

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_Windows 8 桌面應用程式的 AppInit dll 認證需求

Windows 8 傳統型應用程式的其中一項認證需求是，應用程式不能載入任意 dll 來攔截使用 AppInit dll 機制的 WIN32 API 呼叫 \_ 。 如需有關認證需求的詳細資訊，請參閱[Windows 8 傳統型應用程式的認證需求](../win_cert/certification-requirements-for-windows-desktop-apps.md)1.1 一節。

## <a name="summary"></a>摘要

-   AppInit \_ dll 機制不是合法應用程式的建議方法，因為它可能會導致系統鎖死和效能問題。
-   \_啟用安全開機時，預設會停用 AppInit dll 機制。
-   \_在 Windows 8 傳統型應用程式中使用 AppInit dll 是 Windows 的桌面應用程式認證失敗。

請參閱下列白皮書，以取得 \_ Windows 7 和 Windows server 2008 r2 上的 AppInit dll 相關資訊： [Windows 7 和 Windows Server 2008 r2 中的 AppInit dll](/previous-versions/windows/hardware/download/dn550976(v=vs.85))。

 

 
