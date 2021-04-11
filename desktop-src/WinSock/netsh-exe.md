---
description: 適用于 IPv6 的 Netsh 命令提供命令列工具，可讓您用來查詢和設定 IPv6 介面、位址、快取和路由。 Windows XP Service Pack 1 (SP1) 和更新版本支援 Netsh 介面 IPv6 命令。
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113029"
---
# <a name="netshexe"></a><span data-ttu-id="1ef67-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="1ef67-104">Netsh.exe</span></span>

<span data-ttu-id="1ef67-105">適用于 IPv6 的 Netsh 命令提供命令列工具，可讓您用來查詢和設定 IPv6 介面、位址、快取和路由。</span><span class="sxs-lookup"><span data-stu-id="1ef67-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="1ef67-106">Windows XP Service Pack 1 (SP1) 和更新版本支援 Netsh 介面 IPv6 命令。</span><span class="sxs-lookup"><span data-stu-id="1ef67-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="1ef67-107">Netsh.exe 有許多適用于 IPv6 的子命令。</span><span class="sxs-lookup"><span data-stu-id="1ef67-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="1ef67-108">您可以從 Windows XP SP1 和更新版本上的命令提示字元中，輸入下列命令，以取得 Netsh Interface IPv6 的完整選項清單：</span><span class="sxs-lookup"><span data-stu-id="1ef67-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="1ef67-109">**netsh interface ipv6/？**</span><span class="sxs-lookup"><span data-stu-id="1ef67-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="1ef67-110">有關 IPv6 的所有 **netsh** 命令的檔，也可以在 Technet 上線上取得。</span><span class="sxs-lookup"><span data-stu-id="1ef67-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="1ef67-111">如需 Windows Server 2008 上的 **netsh** 的詳細資訊，請參閱 [ (IPv4 和 IPv6) 介面的 netsh 命令](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="1ef67-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="1ef67-112">如需 Windows Server 2003 上 **netsh** 的詳細資訊，請參閱 [介面 IPv6 的 netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="1ef67-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="1ef67-113">以下是一些用於 IPv6 的常用命令，雖然支援許多其他命令：</span><span class="sxs-lookup"><span data-stu-id="1ef67-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="1ef67-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 新增位址**</span><span class="sxs-lookup"><span data-stu-id="1ef67-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-115">將 IPv6 位址新增至本機電腦上的特定介面。</span><span class="sxs-lookup"><span data-stu-id="1ef67-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="1ef67-116">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span><span class="sxs-lookup"><span data-stu-id="1ef67-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-118">針對本機電腦上指定的介面，將 DNS 伺服器 IPv6 位址新增至靜態設定的 DNS 伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="1ef67-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="1ef67-119">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span><span class="sxs-lookup"><span data-stu-id="1ef67-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-121">在本機電腦上新增指定 IPv6 首碼位址的路由。</span><span class="sxs-lookup"><span data-stu-id="1ef67-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="1ef67-122">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh 介面 ipv6 刪除位址**</span><span class="sxs-lookup"><span data-stu-id="1ef67-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-124">從本機電腦上的特定介面刪除指定的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1ef67-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="1ef67-125">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span><span class="sxs-lookup"><span data-stu-id="1ef67-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-127">從靜態設定的 DNS 伺服器清單中，刪除本機電腦上指定之介面的 dns 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="1ef67-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="1ef67-128">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete 介面**</span><span class="sxs-lookup"><span data-stu-id="1ef67-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-130">從本機電腦上的 IPv6 堆疊中刪除指定的介面。</span><span class="sxs-lookup"><span data-stu-id="1ef67-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="1ef67-131">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh 介面 ipv6 刪除路由**</span><span class="sxs-lookup"><span data-stu-id="1ef67-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-133">刪除本機電腦上指定之 IPv6 首碼位址的路由。</span><span class="sxs-lookup"><span data-stu-id="1ef67-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="1ef67-134">此命令具有必須指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span><span class="sxs-lookup"><span data-stu-id="1ef67-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-136">建立腳本，其中包含用來建立目前設定的命令。</span><span class="sxs-lookup"><span data-stu-id="1ef67-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="1ef67-137">如果儲存到檔案中，此指令碼即可用來還原已變更的組態設定。</span><span class="sxs-lookup"><span data-stu-id="1ef67-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 安裝**</span><span class="sxs-lookup"><span data-stu-id="1ef67-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-139">在本機電腦上安裝 IPv6 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1ef67-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 更新**</span><span class="sxs-lookup"><span data-stu-id="1ef67-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-141">重新開機本機電腦上的 IPv6 介面。</span><span class="sxs-lookup"><span data-stu-id="1ef67-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh 介面 ipv6 重設**</span><span class="sxs-lookup"><span data-stu-id="1ef67-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-143">重設本機電腦上的 IPv6 設定狀態。</span><span class="sxs-lookup"><span data-stu-id="1ef67-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span><span class="sxs-lookup"><span data-stu-id="1ef67-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-145">顯示本機電腦上 IPv6 的全域設定參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show 位址**</span><span class="sxs-lookup"><span data-stu-id="1ef67-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-147">顯示本機電腦上特定介面上的所有 IPv6 位址或所有 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1ef67-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="1ef67-148">此命令有可能需要指定的子選項參數。</span><span class="sxs-lookup"><span data-stu-id="1ef67-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="1ef67-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh 介面 ipv6 卸載**</span><span class="sxs-lookup"><span data-stu-id="1ef67-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="1ef67-150">卸載本機電腦上的 IPv6 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1ef67-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="1ef67-151">適用于 IPv4 的 Netsh 命令</span><span class="sxs-lookup"><span data-stu-id="1ef67-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="1ef67-152">IPv4 有類似的 Netsh 命令。</span><span class="sxs-lookup"><span data-stu-id="1ef67-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="1ef67-153">您可以從 Windows XP SP1 和更新版本上的命令提示字元中，輸入下列命令，以取得適用于 IPv4 之 Netsh 命令的完整清單選項：</span><span class="sxs-lookup"><span data-stu-id="1ef67-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="1ef67-154">**netsh interface ip/？**</span><span class="sxs-lookup"><span data-stu-id="1ef67-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="1ef67-155">您也可以在 Technet 上線上取得所有適用于 IPv4 的 Netsh 命令檔。</span><span class="sxs-lookup"><span data-stu-id="1ef67-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="1ef67-156">如需詳細資訊，請參閱 [介面 IP 的 Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="1ef67-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
