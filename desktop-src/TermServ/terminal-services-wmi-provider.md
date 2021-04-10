---
title: 遠端桌面服務 WMI 提供者
description: 遠端桌面服務 WMI 提供者可透過程式設計的方式，存取遠端桌面服務設定/連線 Microsoft Management Console (MMC) 嵌入式管理單元所公開的資訊和設定。
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023639"
---
# <a name="remote-desktop-services-wmi-provider"></a>遠端桌面服務 WMI 提供者

遠端桌面服務 WMI 提供者可透過程式設計的方式，存取遠端桌面服務設定/連線 Microsoft Management Console (MMC) 嵌入式管理單元所公開的資訊和設定。

當用戶端向伺服器提出要求時，Windows 管理進程會將提供者 DLL 載入 (Winmgmt.exe) 。 您可以使用提供者方法來管理。 提供者同時註冊為實例和方法提供者。

遠端桌面服務 WMI 提供者已實作為衍生自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 基類的動態提供者、繼承其所有屬性和方法，以及同進程動態連結程式庫。

如需詳細資訊，請參閱 [遠端桌面服務 WMI 提供者參考](terminal-services-wmi-provider-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遠端桌面服務 WMI 提供者參考](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 