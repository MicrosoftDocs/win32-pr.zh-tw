---
description: 您可以在應用程式的 Windows Installer 套件中設定特定安裝程式屬性的值，以提供在主控台中設定 [新增/移除程式] 所需的所有資訊。
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: 使用 Windows Installer 設定新增/移除程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/30/2021
ms.locfileid: "106995126"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="19dbd-103">使用 Windows Installer 設定新增/移除程式</span><span class="sxs-lookup"><span data-stu-id="19dbd-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="19dbd-104">您可以在應用程式的 Windows Installer 套件中設定特定安裝程式屬性的值，以提供在主控台中設定 [新增/移除程式] 所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="19dbd-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="19dbd-105">設定這些屬性會自動將對應的值寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="19dbd-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="19dbd-106">如果安裝程式偵測到產品已標示為完整移除，則會自動將作業新增至腳本，以移除產品主控台資訊中的 [新增/移除程式] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="19dbd-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="19dbd-107">如果未註冊應用程式，則不會在主控台的 [新增/移除程式] 中列出。</span><span class="sxs-lookup"><span data-stu-id="19dbd-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="19dbd-108">如需詳細資訊，請參閱 [新增和移除應用程式，並在登錄中保留沒有追蹤](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="19dbd-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="19dbd-109">已安裝在每個使用者 [安裝內容](installation-context.md) 中的應用程式會顯示在目前使用者的 [新增/移除程式] 中。</span><span class="sxs-lookup"><span data-stu-id="19dbd-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="19dbd-110">安裝在每部電腦安裝內容中的應用程式會顯示在所有使用者的 [新增/移除程式] 中。</span><span class="sxs-lookup"><span data-stu-id="19dbd-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="19dbd-111">如果應用程式未安裝在每部電腦上，而且僅針對目前使用者以外的使用者安裝為每個使用者的應用程式，則不會出現在目前使用者的 [新增/移除程式] 中。</span><span class="sxs-lookup"><span data-stu-id="19dbd-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="19dbd-112">請注意，使用 [**LIMITUI**](limitui.md) 屬性的安裝套件也必須包含 [**ARPNOMODIFY**](arpnomodify.md)。</span><span class="sxs-lookup"><span data-stu-id="19dbd-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="19dbd-113">若要在嘗試設定產品時，讓使用者從主控台公用程式中的 [新增/移除程式] 取得正確的行為，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="19dbd-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="19dbd-114">安裝程式會使用下列 [公用屬性](public-properties.md) 來管理主控台中的 [新增/移除程式]。</span><span class="sxs-lookup"><span data-stu-id="19dbd-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19dbd-115">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="19dbd-115">Property name</span></span></th>
<th><span data-ttu-id="19dbd-116">屬性的簡短描述</span><span class="sxs-lookup"><span data-stu-id="19dbd-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19dbd-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-118">應用程式更新通道的 URL。</span><span class="sxs-lookup"><span data-stu-id="19dbd-118">URL of the update channel for the application.</span></span> <span data-ttu-id="19dbd-119">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-121">提供主控台中的 [新增/移除程式] 的批註。</span><span class="sxs-lookup"><span data-stu-id="19dbd-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="19dbd-122">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-124">提供主控台中的 [新增/移除程式] 的連絡人。</span><span class="sxs-lookup"><span data-stu-id="19dbd-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="19dbd-125">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-127">應用程式主要資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="19dbd-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="19dbd-128">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-130">技術支援的網際網路位址或 URL。</span><span class="sxs-lookup"><span data-stu-id="19dbd-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="19dbd-131">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-133">技術支援電話號碼。</span><span class="sxs-lookup"><span data-stu-id="19dbd-133">Technical support phone numbers.</span></span> <span data-ttu-id="19dbd-134">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-136">防止在主控台的 [新增/移除程式] 中顯示產品的變更按鈕。</span><span class="sxs-lookup"><span data-stu-id="19dbd-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="19dbd-137">
<b>注意：</b> 這只會影響 ARP 中的顯示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="19dbd-138">Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dbd-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-140">防止在主控台的 [新增/移除程式] 中顯示產品的 [移除] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="19dbd-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="19dbd-141">如果已使用可提供產品移除選項的使用者介面來撰寫安裝套件，仍然可以藉由選取 [變更] 按鈕來移除產品。</span><span class="sxs-lookup"><span data-stu-id="19dbd-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="19dbd-142">
<b>注意：</b> 這只會影響 ARP 中的顯示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="19dbd-143">Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dbd-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-145">在主控台中停用 [新增/移除程式] 中的 [修復] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="19dbd-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="19dbd-146">
<b>注意：</b> 這只會影響 ARP 中的顯示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="19dbd-147">Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dbd-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-149">識別 [新增/移除程式] 中顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="19dbd-150">如果未定義此屬性，[新增/移除程式] 會指定顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-152">提供主控台中的 [新增/移除程式] 的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="19dbd-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="19dbd-153">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-155">應用程式的估計大小（以 KB 為單位）。</span><span class="sxs-lookup"><span data-stu-id="19dbd-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-157">防止在主控台的 [新增/移除程式] 的 [程式] 清單中顯示應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dbd-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="19dbd-158">
<b>注意：</b> 這只會影響 ARP 中的顯示。</span><span class="sxs-lookup"><span data-stu-id="19dbd-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="19dbd-159">Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="19dbd-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19dbd-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-161">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="19dbd-161">URL for application's home page.</span></span> <span data-ttu-id="19dbd-162">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19dbd-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="19dbd-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="19dbd-164">應用程式更新資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="19dbd-164">URL for application update information.</span></span> <span data-ttu-id="19dbd-165">安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。</span><span class="sxs-lookup"><span data-stu-id="19dbd-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="19dbd-166">如需 [設定程式] 和 [預設值] 工具的相關資訊，請參閱 [使用設定程式存取和電腦預設值](/previous-versions//bb776877(v=vs.85))一節。</span><span class="sxs-lookup"><span data-stu-id="19dbd-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19dbd-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="19dbd-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19dbd-168">卸載登錄機碼</span><span class="sxs-lookup"><span data-stu-id="19dbd-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
