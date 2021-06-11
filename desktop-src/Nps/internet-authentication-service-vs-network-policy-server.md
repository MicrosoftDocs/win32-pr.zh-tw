---
title: 網際網路驗證服務 & 網路原則伺服器
description: 瞭解網際網路驗證服務和網路原則伺服器。 網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989423"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="008ef-104">網際網路驗證服務 & 網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="008ef-104">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="008ef-105">網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="008ef-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="008ef-106">網際網路驗證服務</span><span class="sxs-lookup"><span data-stu-id="008ef-106">Internet Authentication Service</span></span>

<span data-ttu-id="008ef-107">網際網路驗證服務是 Microsoft 對 RADIUS 伺服器和 proxy 的實作為。</span><span class="sxs-lookup"><span data-stu-id="008ef-107">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="008ef-108">網際網路驗證服務支援兩個 API 集： [網路原則伺服器延伸 api](ias-extensions.md) 和 [伺服器資料物件 API](server-data-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="008ef-108">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="008ef-109">如需有關 IAS 的詳細資訊，請參閱 [TechNet： Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) 。</span><span class="sxs-lookup"><span data-stu-id="008ef-109">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="008ef-110">網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="008ef-110">Network Policy Server</span></span>

<span data-ttu-id="008ef-111">網路原則伺服器是 Microsoft 對 RADIUS 伺服器和 proxy 的實施，在從 Windows Server 2008 開始的 Windows 伺服器上也可以使用。</span><span class="sxs-lookup"><span data-stu-id="008ef-111">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="008ef-112">NPS 支援與 IAS 相同的兩個 API 集： [網路原則伺服器延伸 api](ias-extensions.md) 和 [伺服器資料物件 API](server-data-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="008ef-112">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="008ef-113">此外，NPS 還包含一組擴充 IAS 功能的新功能。</span><span class="sxs-lookup"><span data-stu-id="008ef-113">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="008ef-114">功能</span><span class="sxs-lookup"><span data-stu-id="008ef-114">Feature</span></span></th>
<th><span data-ttu-id="008ef-115">NPS 的新功能</span><span class="sxs-lookup"><span data-stu-id="008ef-115">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="008ef-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">網路存取保護 (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="008ef-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="008ef-117">NPS 是網路存取保護的中央伺服器。</span><span class="sxs-lookup"><span data-stu-id="008ef-117">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="008ef-118">NPS 支援使用下列其他條件來撰寫原則：</span><span class="sxs-lookup"><span data-stu-id="008ef-118">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="008ef-119">原則到期日。</span><span class="sxs-lookup"><span data-stu-id="008ef-119">Policy expiration.</span></span></li>
<li><span data-ttu-id="008ef-120">作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="008ef-120">Operating system version.</span></span></li>
<li><span data-ttu-id="008ef-121">存取用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="008ef-121">Access client IP address.</span></span></li>
<li><span data-ttu-id="008ef-122">健康原則。</span><span class="sxs-lookup"><span data-stu-id="008ef-122">Health policies.</span></span></li>
<li><span data-ttu-id="008ef-123">允許的 EAP 類型。</span><span class="sxs-lookup"><span data-stu-id="008ef-123">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="008ef-124">HCAP.</span><span class="sxs-lookup"><span data-stu-id="008ef-124">HCAP.</span></span></li>
</ul>
<span data-ttu-id="008ef-125">NPS 支援使用下列其他設定來撰寫原則：</span><span class="sxs-lookup"><span data-stu-id="008ef-125">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="008ef-126">緩刑。</span><span class="sxs-lookup"><span data-stu-id="008ef-126">Probation.</span></span></li>
<li><span data-ttu-id="008ef-127">有限的存取權。</span><span class="sxs-lookup"><span data-stu-id="008ef-127">Limited access.</span></span></li>
<li><span data-ttu-id="008ef-128">限制存取的擴充狀態。</span><span class="sxs-lookup"><span data-stu-id="008ef-128">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="008ef-129">透過 NAP 與 CISCO NAC 互通的 NPS。</span><span class="sxs-lookup"><span data-stu-id="008ef-129">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="008ef-130">IAS 不支援 NAP。</span><span class="sxs-lookup"><span data-stu-id="008ef-130">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008ef-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> 原則和 <a href="/windows/win32/eaphost/portal">EAPHost</a> 支援</span><span class="sxs-lookup"><span data-stu-id="008ef-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="008ef-132">NPS 使用 EAPHost 來進行 EAP 方法擴充性。</span><span class="sxs-lookup"><span data-stu-id="008ef-132">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="008ef-133">此外，系統管理員也可以設定 EAP 的網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="008ef-133">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="008ef-134">IAS 不支援 EAPHost 整合或原則的 EAP 類型篩選準則。</span><span class="sxs-lookup"><span data-stu-id="008ef-134">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008ef-135">IPv6 支援</span><span class="sxs-lookup"><span data-stu-id="008ef-135">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="008ef-136">NPS 支援 IPv6 環境中的部署。</span><span class="sxs-lookup"><span data-stu-id="008ef-136">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="008ef-137">IAS 不支援 IPv6 網路位址。</span><span class="sxs-lookup"><span data-stu-id="008ef-137">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008ef-138">XML 設定</span><span class="sxs-lookup"><span data-stu-id="008ef-138">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="008ef-139">NPS 設定可以用 XML 格式匯入和匯出。</span><span class="sxs-lookup"><span data-stu-id="008ef-139">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="008ef-140">IAS 會使用 Jet 資料庫來儲存服務設定。</span><span class="sxs-lookup"><span data-stu-id="008ef-140">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008ef-141"><a href="https://www.niap-ccevs.org/cc-scheme/">一般準則</a> 支援</span><span class="sxs-lookup"><span data-stu-id="008ef-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="008ef-142">NPS 已更新，可在必須符合通用準則安全性標準的環境中支援其部署。</span><span class="sxs-lookup"><span data-stu-id="008ef-142">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008ef-143"><a href="ias-extensions.md">NPS 擴充功能 API</a></span><span class="sxs-lookup"><span data-stu-id="008ef-143"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="008ef-144">NPS 擴充 Dll 會在與 NPS 服務不同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="008ef-144">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="008ef-145">如果延伸模組 DLL 損毀，NPS 將會繼續執行，且未來的要求將會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="008ef-145">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="008ef-146">IAS 擴充 Dll 會在與 IAS 服務相同的進程中執行，而且可能會對服務造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="008ef-146">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008ef-147">管理消費者介面</span><span class="sxs-lookup"><span data-stu-id="008ef-147">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="008ef-148">Nps 管理主控台 (的 nps) 具有新的外觀、改良的可用性，並涵蓋所有新增至 NPS 的新功能。</span><span class="sxs-lookup"><span data-stu-id="008ef-148">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="008ef-149">IAS 會使用 services.msc 管理主控台。</span><span class="sxs-lookup"><span data-stu-id="008ef-149">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008ef-150">角色管理工具和伺服器管理員整合</span><span class="sxs-lookup"><span data-stu-id="008ef-150">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="008ef-151">NPS 與伺服器管理員和角色管理工具整合。</span><span class="sxs-lookup"><span data-stu-id="008ef-151">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="008ef-152">這項整合可協助您設定和管理 NPS 以及相關的案例。</span><span class="sxs-lookup"><span data-stu-id="008ef-152">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="008ef-153">執行 IAS 的電腦上無法使用伺服器管理員。</span><span class="sxs-lookup"><span data-stu-id="008ef-153">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="008ef-154">已更新 <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>的命令列腳本。</span><span class="sxs-lookup"><span data-stu-id="008ef-154">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="008ef-155">NPS 支援 &quot; Netsh nps &quot; 命令列介面。</span><span class="sxs-lookup"><span data-stu-id="008ef-155">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="008ef-156">&quot;Netsh nps &quot; 包含允許完整設定 nps 的新命令，包括 NAP 功能。</span><span class="sxs-lookup"><span data-stu-id="008ef-156">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="008ef-157">IAS 支援 &quot; Netsh aaaa &quot; 命令列介面。</span><span class="sxs-lookup"><span data-stu-id="008ef-157">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="008ef-158">原則隔離</span><span class="sxs-lookup"><span data-stu-id="008ef-158">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="008ef-159">NPS 可設定網路原則來源，藉此實現原則隔離。</span><span class="sxs-lookup"><span data-stu-id="008ef-159">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="008ef-160">原則可以設定為僅適用于預先決定的 NAS 類型。</span><span class="sxs-lookup"><span data-stu-id="008ef-160">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="008ef-161">IAS 不支援原則隔離。</span><span class="sxs-lookup"><span data-stu-id="008ef-161">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="008ef-162">如需 NPS 的詳細資訊，請參閱 [TechNet：網路原則伺服器](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) 。</span><span class="sxs-lookup"><span data-stu-id="008ef-162">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="008ef-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="008ef-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="008ef-164">RADIUS 驗證、授權和帳戶處理</span><span class="sxs-lookup"><span data-stu-id="008ef-164">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="008ef-165">使用網路原則伺服器進行記錄</span><span class="sxs-lookup"><span data-stu-id="008ef-165">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="008ef-166">使用狀態伺服器</span><span class="sxs-lookup"><span data-stu-id="008ef-166">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

