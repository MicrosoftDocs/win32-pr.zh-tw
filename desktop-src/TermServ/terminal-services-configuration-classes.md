---
title: 遠端桌面服務設定類別
description: 遠端桌面服務設定 WMI 提供者提供下列類別。 如下圖所示。
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375405"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="5700c-104">遠端桌面服務設定類別</span><span class="sxs-lookup"><span data-stu-id="5700c-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="5700c-105">遠端桌面服務設定 WMI 提供者提供下列類別。</span><span class="sxs-lookup"><span data-stu-id="5700c-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="5700c-106">如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5700c-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5700c-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="5700c-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5700c-108">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-109">代表 managed 系統專案與其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5700c-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-110">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5700c-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="5700c-111">代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。</span><span class="sxs-lookup"><span data-stu-id="5700c-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-112">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="5700c-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="5700c-113">System 元素階層的基類。</span><span class="sxs-lookup"><span data-stu-id="5700c-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-114">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="5700c-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="5700c-115">代表一或多個 managed 系統元素的設定相關和指令引數。</span><span class="sxs-lookup"><span data-stu-id="5700c-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-116">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="5700c-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="5700c-117">表示終端。</span><span class="sxs-lookup"><span data-stu-id="5700c-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-118">**Win32 \_ TerminalError**</span><span class="sxs-lookup"><span data-stu-id="5700c-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="5700c-119">表示終端機錯誤。</span><span class="sxs-lookup"><span data-stu-id="5700c-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-120">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="5700c-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="5700c-121">[**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="5700c-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="5700c-122">[**Win32 \_TerminalService**](win32-terminalservice.md)代表 [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **Element** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5700c-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-123">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="5700c-124">代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-125">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="5700c-126">表示 [**Win32 \_ TerminalService**](win32-terminalservice.md) 類別的實例與特定 [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) 屬性的設定之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5700c-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-127">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-128">表示可以套用至終端機的設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-129">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-130">表示終端機與其設定之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5700c-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-131">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="5700c-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="5700c-132">允許刪除存在於 [**Win32 \_ 終端**](win32-terminal.md) 機上的帳戶，以及修改現有的許可權。</span><span class="sxs-lookup"><span data-stu-id="5700c-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-133">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-134">定義與連接原則相關的 [**Win32 \_ 終端**](win32-terminal.md) 機類別的設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-135">**Win32 \_ TSDiscoveredLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5700c-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="5700c-136">提供探索到的遠端桌面授權伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5700c-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-137">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-138">定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的配置設定，包括初始程式原則。</span><span class="sxs-lookup"><span data-stu-id="5700c-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-139">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-140">代表終端機的一般設定，例如加密層級和傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5700c-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-141">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-142">定義與用戶端登入相關的 [**Win32 \_ 終端**](win32-terminal.md) 機類別的配置設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-143">**Win32 \_ TSNetworkAdapterListSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-144">根據指定的終端通訊協定和傳輸方法，列舉可針對 [**Win32 \_ 終端**](win32-terminal.md)機設定的網路介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="5700c-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-145">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="5700c-146">定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的各種設定，包括與網路介面卡相關的屬性，以及允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="5700c-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-147">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="5700c-148">包含將新帳戶新增至終端機的方法，以及將預設許可權還原到終端機的方法。</span><span class="sxs-lookup"><span data-stu-id="5700c-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-149">**Win32 \_ TSRemoteControlSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-150">定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的遠端控制設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-151">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="5700c-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="5700c-152">定義 [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) 類別的遠端桌面連線代理人 (RD 連線代理人) 設定。</span><span class="sxs-lookup"><span data-stu-id="5700c-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-153">**Win32 \_ TSSessionDirectorySetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="5700c-154">表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 類別的實例與 [**win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) 類別的實例之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5700c-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-155">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-156">定義 [**Win32 \_ 終端**](win32-terminal.md) 機類別的設定，例如時間限制以及中斷連線和重新連接動作。</span><span class="sxs-lookup"><span data-stu-id="5700c-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-157">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="5700c-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="5700c-158">定義 RD 工作階段主機伺服器 (IP) 虛擬化設定的網際網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5700c-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="5700c-159">**Win32 \_ TSVirtualIPSetting**</span><span class="sxs-lookup"><span data-stu-id="5700c-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="5700c-160">表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 元素類別和 [**win32 \_ TSVirtualIP**](win32-tsvirtualip.md) 設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5700c-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="5700c-161">下圖顯示這些類別之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="5700c-161">The following illustration shows the relationships between these classes.</span></span>

![支援類別之間的關聯性](images/tswmi.png)

 

 