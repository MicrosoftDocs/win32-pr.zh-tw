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
# <a name="netshexe"></a>Netsh.exe

適用于 IPv6 的 Netsh 命令提供命令列工具，可讓您用來查詢和設定 IPv6 介面、位址、快取和路由。 Windows XP Service Pack 1 (SP1) 和更新版本支援 Netsh 介面 IPv6 命令。

Netsh.exe 有許多適用于 IPv6 的子命令。 您可以從 Windows XP SP1 和更新版本上的命令提示字元中，輸入下列命令，以取得 Netsh Interface IPv6 的完整選項清單：

**netsh interface ipv6/？**

有關 IPv6 的所有 **netsh** 命令的檔，也可以在 Technet 上線上取得。 如需 Windows Server 2008 上的 **netsh** 的詳細資訊，請參閱 [ (IPv4 和 IPv6) 介面的 netsh 命令](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10))。 如需 Windows Server 2003 上 **netsh** 的詳細資訊，請參閱 [介面 IPv6 的 netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10))。

以下是一些用於 IPv6 的常用命令，雖然支援許多其他命令：

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 新增位址**
</dt> <dd>

將 IPv6 位址新增至本機電腦上的特定介面。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**
</dt> <dd>

針對本機電腦上指定的介面，將 DNS 伺服器 IPv6 位址新增至靜態設定的 DNS 伺服器清單。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**
</dt> <dd>

在本機電腦上新增指定 IPv6 首碼位址的路由。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh 介面 ipv6 刪除位址**
</dt> <dd>

從本機電腦上的特定介面刪除指定的 IPv6 位址。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**
</dt> <dd>

從靜態設定的 DNS 伺服器清單中，刪除本機電腦上指定之介面的 dns 伺服器位址。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete 介面**
</dt> <dd>

從本機電腦上的 IPv6 堆疊中刪除指定的介面。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh 介面 ipv6 刪除路由**
</dt> <dd>

刪除本機電腦上指定之 IPv6 首碼位址的路由。 此命令具有必須指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**
</dt> <dd>

建立腳本，其中包含用來建立目前設定的命令。 如果儲存到檔案中，此指令碼即可用來還原已變更的組態設定。

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 安裝**
</dt> <dd>

在本機電腦上安裝 IPv6 通訊協定。

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 更新**
</dt> <dd>

重新開機本機電腦上的 IPv6 介面。

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh 介面 ipv6 重設**
</dt> <dd>

重設本機電腦上的 IPv6 設定狀態。

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**
</dt> <dd>

顯示本機電腦上 IPv6 的全域設定參數。

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show 位址**
</dt> <dd>

顯示本機電腦上特定介面上的所有 IPv6 位址或所有 IPv6 位址。 此命令有可能需要指定的子選項參數。

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh 介面 ipv6 卸載**
</dt> <dd>

卸載本機電腦上的 IPv6 通訊協定。

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>適用于 IPv4 的 Netsh 命令

IPv4 有類似的 Netsh 命令。 您可以從 Windows XP SP1 和更新版本上的命令提示字元中，輸入下列命令，以取得適用于 IPv4 之 Netsh 命令的完整清單選項：

**netsh interface ip/？**

您也可以在 Technet 上線上取得所有適用于 IPv4 的 Netsh 命令檔。 如需詳細資訊，請參閱 [介面 IP 的 Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))

 

 
