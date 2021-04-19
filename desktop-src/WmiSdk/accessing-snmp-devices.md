---
description: 允許用戶端應用程式透過 WMI 存取 SNMP 資訊。
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: 存取 SNMP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988479"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="d903d-103">存取 SNMP 裝置</span><span class="sxs-lookup"><span data-stu-id="d903d-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="d903d-104">簡易網路管理通訊協定 (SNMP) 提供者，可讓用戶端應用程式透過 WMI 存取 SNMP 資訊。</span><span class="sxs-lookup"><span data-stu-id="d903d-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="d903d-105">[Snmp 提供者](snmp-provider.md)可作為使用 SNMP 進行管理之系統與裝置的閘道。</span><span class="sxs-lookup"><span data-stu-id="d903d-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="d903d-106">只有管理或監視電腦必須執行 WMI，因為它可以從任何已啟用 SNMP 的裝置讀取。</span><span class="sxs-lookup"><span data-stu-id="d903d-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="d903d-107">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="d903d-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="d903d-108">SNMP 管理資訊基底 (MIB) 物件變數可以從中讀取和寫入，而且 SNMP 陷阱可以自動對應至 WMI 事件，這些事件可以針對任何在 MIB 定義的陷阱以外的資料進行任意建立、刪除或更新作業而定義。</span><span class="sxs-lookup"><span data-stu-id="d903d-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="d903d-109">WMI 功能的這項功能是標準 SNMP 功能的延伸。</span><span class="sxs-lookup"><span data-stu-id="d903d-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="d903d-110">如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。</span><span class="sxs-lookup"><span data-stu-id="d903d-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="d903d-111">下列主題中所述的工具是設計來供 Windows 腳本和 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="d903d-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="d903d-112">建議您熟悉 WMI、SNMPv1 和 SNMPv2C，以及網路和網路管理概念的實用知識。</span><span class="sxs-lookup"><span data-stu-id="d903d-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="d903d-113">如需有關搭配 SNMP 使用 WMI 的詳細資訊，請參閱 [設定 WMI Snmp 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="d903d-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 



