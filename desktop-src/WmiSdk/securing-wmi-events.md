---
description: WMI 事件是由事件提供者傳遞給暫時或永久的取用者。 WMI 事件系統會使用事件和使用者帳戶 Sid 的安全描述項比較來控制事件存取。
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: 保護 WMI 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192071"
---
# <a name="securing-wmi-events"></a>保護 WMI 事件

WMI 事件是由 [*事件提供*](gloss-e.md) 者傳遞給 [*暫時*](gloss-t.md) 或 [*永久*](gloss-p.md) 的取用者。 WMI 事件系統會使用事件和使用者帳戶 [*sid*](gloss-s.md)的 [*安全描述項*](gloss-s.md)比較來控制事件存取。

事件是以事件類別實例的形式傳遞，但不一定是從 [**\_ \_ 事件**](--event.md)最終衍生。 Wmi 提供 [wmi 系統類別](wmi-system-classes.md)中的數個一般事件類別，例如 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)。 提供者也可以提供自己的事件類別。 例如， [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 有事件類別，可報告登錄機碼或值的變更，例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)。

下列主題提供有關安全傳遞提供者的事件，以及安全地針對用戶端腳本和應用程式接收事件的資訊：

-   [安全地提供事件](providing-events-securely.md)
-   [安全地接收事件](receiving-events-securely.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 

 
