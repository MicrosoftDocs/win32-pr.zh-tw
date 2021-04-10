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
# <a name="securing-wmi-events"></a><span data-ttu-id="7ea4d-104">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="7ea4d-104">Securing WMI Events</span></span>

<span data-ttu-id="7ea4d-105">WMI 事件是由 [*事件提供*](gloss-e.md) 者傳遞給 [*暫時*](gloss-t.md) 或 [*永久*](gloss-p.md) 的取用者。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="7ea4d-106">WMI 事件系統會使用事件和使用者帳戶 [*sid*](gloss-s.md)的 [*安全描述項*](gloss-s.md)比較來控制事件存取。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="7ea4d-107">事件是以事件類別實例的形式傳遞，但不一定是從 [**\_ \_ 事件**](--event.md)最終衍生。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="7ea4d-108">Wmi 提供 [wmi 系統類別](wmi-system-classes.md)中的數個一般事件類別，例如 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="7ea4d-109">提供者也可以提供自己的事件類別。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="7ea4d-110">例如， [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 有事件類別，可報告登錄機碼或值的變更，例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)。</span><span class="sxs-lookup"><span data-stu-id="7ea4d-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="7ea4d-111">下列主題提供有關安全傳遞提供者的事件，以及安全地針對用戶端腳本和應用程式接收事件的資訊：</span><span class="sxs-lookup"><span data-stu-id="7ea4d-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="7ea4d-112">安全地提供事件</span><span class="sxs-lookup"><span data-stu-id="7ea4d-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="7ea4d-113">安全地接收事件</span><span class="sxs-lookup"><span data-stu-id="7ea4d-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="7ea4d-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ea4d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea4d-115">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="7ea4d-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
