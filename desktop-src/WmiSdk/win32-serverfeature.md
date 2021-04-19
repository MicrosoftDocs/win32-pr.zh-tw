---
description: Win32 \_ ServerFeature 類別代表安裝在執行 Windows Server 之電腦上的功能。
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987789"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="dfdca-103">Win32 \_ ServerFeature 類別</span><span class="sxs-lookup"><span data-stu-id="dfdca-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="dfdca-104">\[**Win32 \_ ServerFeature** 類別可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="dfdca-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dfdca-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="dfdca-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dfdca-106">相反地，請使用 [ServerManager Deploymentprovider 提供者類別](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)。\]</span><span class="sxs-lookup"><span data-stu-id="dfdca-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="dfdca-107">**Win32 \_ ServerFeature** 類別代表安裝在執行 Windows Server 之電腦上的功能。</span><span class="sxs-lookup"><span data-stu-id="dfdca-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="dfdca-108">開發人員和系統管理員可以使用這個類別，將判斷安裝在一組伺服器電腦上的功能自動化。</span><span class="sxs-lookup"><span data-stu-id="dfdca-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="dfdca-109">用戶端電腦上無法使用這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dfdca-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdca-110">語法</span><span class="sxs-lookup"><span data-stu-id="dfdca-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="dfdca-111">成員</span><span class="sxs-lookup"><span data-stu-id="dfdca-111">Members</span></span>

<span data-ttu-id="dfdca-112">**Win32 \_ ServerFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dfdca-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="dfdca-113">屬性</span><span class="sxs-lookup"><span data-stu-id="dfdca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfdca-114">屬性</span><span class="sxs-lookup"><span data-stu-id="dfdca-114">Properties</span></span>

<span data-ttu-id="dfdca-115">**Win32 \_ ServerFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dfdca-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfdca-116">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="dfdca-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfdca-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfdca-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfdca-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dfdca-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfdca-119">限定詞：索引 [**鍵**](key-qualifier.md)， [**非 \_ Null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dfdca-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dfdca-120">伺服器功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfdca-120">Server feature ID.</span></span> <span data-ttu-id="dfdca-121">下列清單顯示 [識別碼] 屬性的可能值：</span><span class="sxs-lookup"><span data-stu-id="dfdca-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="dfdca-122">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-122">Value</span></span>

<span data-ttu-id="dfdca-123">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-123">Name</span></span>

<span data-ttu-id="dfdca-124">1</span><span class="sxs-lookup"><span data-stu-id="dfdca-124">1</span></span>

[<span data-ttu-id="dfdca-125">應用程式伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-125">Application Server</span></span>](/windows)

<span data-ttu-id="dfdca-126">2</span><span class="sxs-lookup"><span data-stu-id="dfdca-126">2</span></span>

<span data-ttu-id="dfdca-127">Web 伺服器 (IIS)</span><span class="sxs-lookup"><span data-stu-id="dfdca-127">Web Server (IIS)</span></span>

<span data-ttu-id="dfdca-128">3</span><span class="sxs-lookup"><span data-stu-id="dfdca-128">3</span></span>

[<span data-ttu-id="dfdca-129">串流處理媒體服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="dfdca-130">5</span><span class="sxs-lookup"><span data-stu-id="dfdca-130">5</span></span>

<span data-ttu-id="dfdca-131">傳真伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-131">Fax Server</span></span>

<span data-ttu-id="dfdca-132">6</span><span class="sxs-lookup"><span data-stu-id="dfdca-132">6</span></span>

<span data-ttu-id="dfdca-133">檔案和 iSCSI 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="dfdca-134">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-135">7</span><span class="sxs-lookup"><span data-stu-id="dfdca-135">7</span></span>

<span data-ttu-id="dfdca-136">列印和文件服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-136">Print and Document Services</span></span><br/> [<span data-ttu-id="dfdca-137">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-138">8</span><span class="sxs-lookup"><span data-stu-id="dfdca-138">8</span></span>

[<span data-ttu-id="dfdca-139">Active Directory 同盟服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="dfdca-140">9</span><span class="sxs-lookup"><span data-stu-id="dfdca-140">9</span></span>

<span data-ttu-id="dfdca-141">Active Directory 輕量型目錄服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="dfdca-142">10</span><span class="sxs-lookup"><span data-stu-id="dfdca-142">10</span></span>

<span data-ttu-id="dfdca-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-143">Active Directory Domain Services</span></span>

<span data-ttu-id="dfdca-144">11</span><span class="sxs-lookup"><span data-stu-id="dfdca-144">11</span></span>

[<span data-ttu-id="dfdca-145">UDDI 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-146">12</span><span class="sxs-lookup"><span data-stu-id="dfdca-146">12</span></span>

[<span data-ttu-id="dfdca-147">DHCP 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="dfdca-148">13</span><span class="sxs-lookup"><span data-stu-id="dfdca-148">13</span></span>

[<span data-ttu-id="dfdca-149">DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-149">DNS Server</span></span>](/windows)

<span data-ttu-id="dfdca-150">14</span><span class="sxs-lookup"><span data-stu-id="dfdca-150">14</span></span>

<span data-ttu-id="dfdca-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-151">Network Policy and Access Services</span></span>

<span data-ttu-id="dfdca-152">16</span><span class="sxs-lookup"><span data-stu-id="dfdca-152">16</span></span>

<span data-ttu-id="dfdca-153">Active Directory 憑證服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="dfdca-154">17</span><span class="sxs-lookup"><span data-stu-id="dfdca-154">17</span></span>

<span data-ttu-id="dfdca-155">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="dfdca-156">18</span><span class="sxs-lookup"><span data-stu-id="dfdca-156">18</span></span>

[<span data-ttu-id="dfdca-157">遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-158">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-159">19</span><span class="sxs-lookup"><span data-stu-id="dfdca-159">19</span></span>

<span data-ttu-id="dfdca-160">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-160">Windows Deployment Services</span></span>

<span data-ttu-id="dfdca-161">20</span><span class="sxs-lookup"><span data-stu-id="dfdca-161">20</span></span>

<span data-ttu-id="dfdca-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="dfdca-162">Hyper-V</span></span>

<span data-ttu-id="dfdca-163">21</span><span class="sxs-lookup"><span data-stu-id="dfdca-163">21</span></span>

[<span data-ttu-id="dfdca-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="dfdca-165">33</span><span class="sxs-lookup"><span data-stu-id="dfdca-165">33</span></span>

[<span data-ttu-id="dfdca-166">容錯移轉叢集</span><span class="sxs-lookup"><span data-stu-id="dfdca-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="dfdca-167">34</span><span class="sxs-lookup"><span data-stu-id="dfdca-167">34</span></span>

[<span data-ttu-id="dfdca-168">網路負載平衡</span><span class="sxs-lookup"><span data-stu-id="dfdca-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="dfdca-169">36</span><span class="sxs-lookup"><span data-stu-id="dfdca-169">36</span></span>

[<span data-ttu-id="dfdca-170">.NET Framework 3.5.1 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-171">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-172">37</span><span class="sxs-lookup"><span data-stu-id="dfdca-172">37</span></span>

[<span data-ttu-id="dfdca-173">Windows 系統資源管理員</span><span class="sxs-lookup"><span data-stu-id="dfdca-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="dfdca-174">38</span><span class="sxs-lookup"><span data-stu-id="dfdca-174">38</span></span>

<span data-ttu-id="dfdca-175">無線區域網路服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-175">Wireless LAN Service</span></span>

<span data-ttu-id="dfdca-176">39</span><span class="sxs-lookup"><span data-stu-id="dfdca-176">39</span></span>

[<span data-ttu-id="dfdca-177">Windows Server Backup 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="dfdca-178">40</span><span class="sxs-lookup"><span data-stu-id="dfdca-178">40</span></span>

<span data-ttu-id="dfdca-179">WINS 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-179">WINS Server</span></span>

<span data-ttu-id="dfdca-180">41</span><span class="sxs-lookup"><span data-stu-id="dfdca-180">41</span></span>

<span data-ttu-id="dfdca-181">Windows 處理序啟用服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-181">Windows Process Activation Service</span></span>

<span data-ttu-id="dfdca-182">42</span><span class="sxs-lookup"><span data-stu-id="dfdca-182">42</span></span>

[<span data-ttu-id="dfdca-183">遠端協助</span><span class="sxs-lookup"><span data-stu-id="dfdca-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="dfdca-184">43</span><span class="sxs-lookup"><span data-stu-id="dfdca-184">43</span></span>

<span data-ttu-id="dfdca-185">簡單 TCP/IP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="dfdca-186">44</span><span class="sxs-lookup"><span data-stu-id="dfdca-186">44</span></span>

[<span data-ttu-id="dfdca-187">Telnet 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="dfdca-188">45</span><span class="sxs-lookup"><span data-stu-id="dfdca-188">45</span></span>

[<span data-ttu-id="dfdca-189">Telnet 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="dfdca-190">46</span><span class="sxs-lookup"><span data-stu-id="dfdca-190">46</span></span>

[<span data-ttu-id="dfdca-191">以 Unix 為基礎的應用程式子系統</span><span class="sxs-lookup"><span data-stu-id="dfdca-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="dfdca-192">47</span><span class="sxs-lookup"><span data-stu-id="dfdca-192">47</span></span>

<span data-ttu-id="dfdca-193">RPC Over HTTP Proxy</span><span class="sxs-lookup"><span data-stu-id="dfdca-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="dfdca-194">48</span><span class="sxs-lookup"><span data-stu-id="dfdca-194">48</span></span>

<span data-ttu-id="dfdca-195">SMTP 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-195">SMTP Server</span></span>

<span data-ttu-id="dfdca-196">49</span><span class="sxs-lookup"><span data-stu-id="dfdca-196">49</span></span>

<span data-ttu-id="dfdca-197">訊息佇列</span><span class="sxs-lookup"><span data-stu-id="dfdca-197">Message Queuing</span></span>

<span data-ttu-id="dfdca-198">51</span><span class="sxs-lookup"><span data-stu-id="dfdca-198">51</span></span>

[<span data-ttu-id="dfdca-199">Windows 內部資料庫</span><span class="sxs-lookup"><span data-stu-id="dfdca-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="dfdca-200">52</span><span class="sxs-lookup"><span data-stu-id="dfdca-200">52</span></span>

[<span data-ttu-id="dfdca-201">San 存放管理員</span><span class="sxs-lookup"><span data-stu-id="dfdca-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="dfdca-202">53</span><span class="sxs-lookup"><span data-stu-id="dfdca-202">53</span></span>

<span data-ttu-id="dfdca-203">LPR 連接埠監視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-203">LPR Port Monitor</span></span>

<span data-ttu-id="dfdca-204">55</span><span class="sxs-lookup"><span data-stu-id="dfdca-204">55</span></span>

[<span data-ttu-id="dfdca-205">Internet Storage Name Server</span><span class="sxs-lookup"><span data-stu-id="dfdca-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="dfdca-206">57</span><span class="sxs-lookup"><span data-stu-id="dfdca-206">57</span></span>

[<span data-ttu-id="dfdca-207">多重路徑 I/O</span><span class="sxs-lookup"><span data-stu-id="dfdca-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="dfdca-208">58</span><span class="sxs-lookup"><span data-stu-id="dfdca-208">58</span></span>

<span data-ttu-id="dfdca-209">TFTP 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-209">TFTP Client</span></span>

<span data-ttu-id="dfdca-210">59</span><span class="sxs-lookup"><span data-stu-id="dfdca-210">59</span></span>

[<span data-ttu-id="dfdca-211">SNMP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="dfdca-212">60</span><span class="sxs-lookup"><span data-stu-id="dfdca-212">60</span></span>

[<span data-ttu-id="dfdca-213">卸除式存放裝置管理員</span><span class="sxs-lookup"><span data-stu-id="dfdca-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="dfdca-214">61</span><span class="sxs-lookup"><span data-stu-id="dfdca-214">61</span></span>

<span data-ttu-id="dfdca-215">BitLocker 磁碟機加密</span><span class="sxs-lookup"><span data-stu-id="dfdca-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="dfdca-216">62</span><span class="sxs-lookup"><span data-stu-id="dfdca-216">62</span></span>

[<span data-ttu-id="dfdca-217">適用于網路檔案系統的服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="dfdca-218">63</span><span class="sxs-lookup"><span data-stu-id="dfdca-218">63</span></span>

<span data-ttu-id="dfdca-219">網際網路列印用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-219">Internet Printing Client</span></span>

<span data-ttu-id="dfdca-220">64</span><span class="sxs-lookup"><span data-stu-id="dfdca-220">64</span></span>

[<span data-ttu-id="dfdca-221">對等名稱解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="dfdca-222">65</span><span class="sxs-lookup"><span data-stu-id="dfdca-222">65</span></span>

<span data-ttu-id="dfdca-223">連線管理員系統管理組件</span><span class="sxs-lookup"><span data-stu-id="dfdca-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="dfdca-224">66</span><span class="sxs-lookup"><span data-stu-id="dfdca-224">66</span></span>

[<span data-ttu-id="dfdca-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfdca-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-226">67</span><span class="sxs-lookup"><span data-stu-id="dfdca-226">67</span></span>

[<span data-ttu-id="dfdca-227">遠端伺服器管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="dfdca-228">68</span><span class="sxs-lookup"><span data-stu-id="dfdca-228">68</span></span>

[<span data-ttu-id="dfdca-229">高品質 Windows 音訊/視訊體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="dfdca-230">69</span><span class="sxs-lookup"><span data-stu-id="dfdca-230">69</span></span>

[<span data-ttu-id="dfdca-231">群組原則管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="dfdca-232">71</span><span class="sxs-lookup"><span data-stu-id="dfdca-232">71</span></span>

[<span data-ttu-id="dfdca-233">索引服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="dfdca-234">72</span><span class="sxs-lookup"><span data-stu-id="dfdca-234">72</span></span>

[<span data-ttu-id="dfdca-235">檔案伺服器資源管理員 (FSRM)</span><span class="sxs-lookup"><span data-stu-id="dfdca-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="dfdca-236">73</span><span class="sxs-lookup"><span data-stu-id="dfdca-236">73</span></span>

<span data-ttu-id="dfdca-237">遠端差異壓縮</span><span class="sxs-lookup"><span data-stu-id="dfdca-237">Remote Differential Compression</span></span>

<span data-ttu-id="dfdca-238">310</span><span class="sxs-lookup"><span data-stu-id="dfdca-238">310</span></span>

<span data-ttu-id="dfdca-239">筆跡和手寫服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="dfdca-240">320</span><span class="sxs-lookup"><span data-stu-id="dfdca-240">320</span></span>

[<span data-ttu-id="dfdca-241">Windows Server 移轉工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-242">321</span><span class="sxs-lookup"><span data-stu-id="dfdca-242">321</span></span>

[<span data-ttu-id="dfdca-243">WinRM IIS 延伸模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-244">324</span><span class="sxs-lookup"><span data-stu-id="dfdca-244">324</span></span>

[<span data-ttu-id="dfdca-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="dfdca-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="dfdca-246">334</span><span class="sxs-lookup"><span data-stu-id="dfdca-246">334</span></span>

[<span data-ttu-id="dfdca-247">DirectAccess 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-248">335</span><span class="sxs-lookup"><span data-stu-id="dfdca-248">335</span></span>

[<span data-ttu-id="dfdca-249">背景智慧型傳送服務 (BITS)</span><span class="sxs-lookup"><span data-stu-id="dfdca-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-250">338</span><span class="sxs-lookup"><span data-stu-id="dfdca-250">338</span></span>

[<span data-ttu-id="dfdca-251">XPS 檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-252">339</span><span class="sxs-lookup"><span data-stu-id="dfdca-252">339</span></span>

[<span data-ttu-id="dfdca-253">Windows 生物特徵辨識架構</span><span class="sxs-lookup"><span data-stu-id="dfdca-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-254">340</span><span class="sxs-lookup"><span data-stu-id="dfdca-254">340</span></span>

<span data-ttu-id="dfdca-255">WoW64 支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-255">WoW64 Support</span></span><br/>

<span data-ttu-id="dfdca-256">351</span><span class="sxs-lookup"><span data-stu-id="dfdca-256">351</span></span>

[<span data-ttu-id="dfdca-257">Windows PowerShell (ISE) 的整合式腳本環境 </span><span class="sxs-lookup"><span data-stu-id="dfdca-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-258">352</span><span class="sxs-lookup"><span data-stu-id="dfdca-258">352</span></span>

<span data-ttu-id="dfdca-259">Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="dfdca-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="dfdca-260">404</span><span class="sxs-lookup"><span data-stu-id="dfdca-260">404</span></span>

[<span data-ttu-id="dfdca-261">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="dfdca-262">409</span><span class="sxs-lookup"><span data-stu-id="dfdca-262">409</span></span>

[<span data-ttu-id="dfdca-263">IP 位址管理 (IPAM) 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="dfdca-264">417</span><span class="sxs-lookup"><span data-stu-id="dfdca-264">417</span></span>

[<span data-ttu-id="dfdca-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfdca-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="dfdca-266">418</span><span class="sxs-lookup"><span data-stu-id="dfdca-266">418</span></span>

[<span data-ttu-id="dfdca-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="dfdca-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="dfdca-268">432</span><span class="sxs-lookup"><span data-stu-id="dfdca-268">432</span></span>

[<span data-ttu-id="dfdca-269">Windows Search 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="dfdca-270">438</span><span class="sxs-lookup"><span data-stu-id="dfdca-270">438</span></span>

[<span data-ttu-id="dfdca-271">Client for NFS</span><span class="sxs-lookup"><span data-stu-id="dfdca-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="dfdca-272">441</span><span class="sxs-lookup"><span data-stu-id="dfdca-272">441</span></span>

[<span data-ttu-id="dfdca-273">BitLocker 網路解除鎖定</span><span class="sxs-lookup"><span data-stu-id="dfdca-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="dfdca-274">442</span><span class="sxs-lookup"><span data-stu-id="dfdca-274">442</span></span>

[<span data-ttu-id="dfdca-275">Management OData IIS 延伸模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="dfdca-276">450</span><span class="sxs-lookup"><span data-stu-id="dfdca-276">450</span></span>

[<span data-ttu-id="dfdca-277">.NET Framework 4.5 進階服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="dfdca-278">466</span><span class="sxs-lookup"><span data-stu-id="dfdca-278">466</span></span>

[<span data-ttu-id="dfdca-279">.NET Framework 4.5 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="dfdca-280">468</span><span class="sxs-lookup"><span data-stu-id="dfdca-280">468</span></span>

[<span data-ttu-id="dfdca-281">遠端存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-282">477</span><span class="sxs-lookup"><span data-stu-id="dfdca-282">477</span></span>

[<span data-ttu-id="dfdca-283">使用者介面和基礎結構</span><span class="sxs-lookup"><span data-stu-id="dfdca-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="dfdca-284">478</span><span class="sxs-lookup"><span data-stu-id="dfdca-284">478</span></span>

[<span data-ttu-id="dfdca-285">圖形化管理工具與基礎結構</span><span class="sxs-lookup"><span data-stu-id="dfdca-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="dfdca-286">481</span><span class="sxs-lookup"><span data-stu-id="dfdca-286">481</span></span>

[<span data-ttu-id="dfdca-287">檔案和存放服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="dfdca-288">485</span><span class="sxs-lookup"><span data-stu-id="dfdca-288">485</span></span>

[<span data-ttu-id="dfdca-289">Windows Server Essentials 體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="dfdca-290">488</span><span class="sxs-lookup"><span data-stu-id="dfdca-290">488</span></span>

[<span data-ttu-id="dfdca-291">Direct Play</span><span class="sxs-lookup"><span data-stu-id="dfdca-291">Direct Play</span></span>](/windows)

<span data-ttu-id="dfdca-292">檔案服務-角色服務 (6) </span><span class="sxs-lookup"><span data-stu-id="dfdca-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="dfdca-293">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-293">Value</span></span>

<span data-ttu-id="dfdca-294">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-294">Name</span></span>

<span data-ttu-id="dfdca-295">100</span><span class="sxs-lookup"><span data-stu-id="dfdca-295">100</span></span>

[<span data-ttu-id="dfdca-296">分散式檔案系統</span><span class="sxs-lookup"><span data-stu-id="dfdca-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="dfdca-297">101</span><span class="sxs-lookup"><span data-stu-id="dfdca-297">101</span></span>

<span data-ttu-id="dfdca-298">DFS 命名空間</span><span class="sxs-lookup"><span data-stu-id="dfdca-298">DFS Namespace</span></span>

<span data-ttu-id="dfdca-299">102</span><span class="sxs-lookup"><span data-stu-id="dfdca-299">102</span></span>

<span data-ttu-id="dfdca-300">DFS 複寫</span><span class="sxs-lookup"><span data-stu-id="dfdca-300">DFS Replication</span></span>

<span data-ttu-id="dfdca-301">103</span><span class="sxs-lookup"><span data-stu-id="dfdca-301">103</span></span>

[<span data-ttu-id="dfdca-302">檔案複寫服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="dfdca-303">104</span><span class="sxs-lookup"><span data-stu-id="dfdca-303">104</span></span>

[<span data-ttu-id="dfdca-304">檔案伺服器資源管理員 (FSRM)</span><span class="sxs-lookup"><span data-stu-id="dfdca-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="dfdca-305">105</span><span class="sxs-lookup"><span data-stu-id="dfdca-305">105</span></span>

[<span data-ttu-id="dfdca-306">適用于網路檔案系統的服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="dfdca-307">106</span><span class="sxs-lookup"><span data-stu-id="dfdca-307">106</span></span>

[<span data-ttu-id="dfdca-308">儲存單一版本</span><span class="sxs-lookup"><span data-stu-id="dfdca-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="dfdca-309">107</span><span class="sxs-lookup"><span data-stu-id="dfdca-309">107</span></span>

[<span data-ttu-id="dfdca-310">Windows Search 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="dfdca-311">108</span><span class="sxs-lookup"><span data-stu-id="dfdca-311">108</span></span>

[<span data-ttu-id="dfdca-312">索引服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="dfdca-313">255</span><span class="sxs-lookup"><span data-stu-id="dfdca-313">255</span></span>

<span data-ttu-id="dfdca-314">檔案伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-314">File Server</span></span>

<span data-ttu-id="dfdca-315">350</span><span class="sxs-lookup"><span data-stu-id="dfdca-315">350</span></span>

<span data-ttu-id="dfdca-316">網路檔案的 BranchCache</span><span class="sxs-lookup"><span data-stu-id="dfdca-316">BranchCache for Network Files</span></span>

<span data-ttu-id="dfdca-317">431</span><span class="sxs-lookup"><span data-stu-id="dfdca-317">431</span></span>

[<span data-ttu-id="dfdca-318">NFS 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-319">434</span><span class="sxs-lookup"><span data-stu-id="dfdca-319">434</span></span>

[<span data-ttu-id="dfdca-320">檔案伺服器 VSS 代理程式服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-321">435</span><span class="sxs-lookup"><span data-stu-id="dfdca-321">435</span></span>

[<span data-ttu-id="dfdca-322">iSCSI 目標伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-323">436</span><span class="sxs-lookup"><span data-stu-id="dfdca-323">436</span></span>

[<span data-ttu-id="dfdca-324">重複資料刪除</span><span class="sxs-lookup"><span data-stu-id="dfdca-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-325">437</span><span class="sxs-lookup"><span data-stu-id="dfdca-325">437</span></span>

[<span data-ttu-id="dfdca-326">iSCSI 目標儲存提供者 (VDS 和 VSS 硬體提供者) </span><span class="sxs-lookup"><span data-stu-id="dfdca-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="dfdca-327">486</span><span class="sxs-lookup"><span data-stu-id="dfdca-327">486</span></span>

[<span data-ttu-id="dfdca-328">工作資料夾</span><span class="sxs-lookup"><span data-stu-id="dfdca-328">Work Folders</span></span>](/windows)

<span data-ttu-id="dfdca-329">AD DS-角色服務 (10) </span><span class="sxs-lookup"><span data-stu-id="dfdca-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="dfdca-330">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-330">Value</span></span>

<span data-ttu-id="dfdca-331">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-331">Name</span></span>

<span data-ttu-id="dfdca-332">110</span><span class="sxs-lookup"><span data-stu-id="dfdca-332">110</span></span>

[<span data-ttu-id="dfdca-333">Active Directory 網域控制站</span><span class="sxs-lookup"><span data-stu-id="dfdca-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="dfdca-334">111</span><span class="sxs-lookup"><span data-stu-id="dfdca-334">111</span></span>

[<span data-ttu-id="dfdca-335">Unix 身分識別管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="dfdca-336">112</span><span class="sxs-lookup"><span data-stu-id="dfdca-336">112</span></span>

[<span data-ttu-id="dfdca-337">網路資訊服務的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="dfdca-338">113</span><span class="sxs-lookup"><span data-stu-id="dfdca-338">113</span></span>

[<span data-ttu-id="dfdca-339">密碼同步</span><span class="sxs-lookup"><span data-stu-id="dfdca-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="dfdca-340">294</span><span class="sxs-lookup"><span data-stu-id="dfdca-340">294</span></span>

[<span data-ttu-id="dfdca-341">遠端伺服器管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="dfdca-342">串流處理媒體-角色服務 (3) </span><span class="sxs-lookup"><span data-stu-id="dfdca-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="dfdca-343">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-343">Value</span></span>

<span data-ttu-id="dfdca-344">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-344">Name</span></span>

<span data-ttu-id="dfdca-345">120</span><span class="sxs-lookup"><span data-stu-id="dfdca-345">120</span></span>

[<span data-ttu-id="dfdca-346">Windows Media 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="dfdca-347">121</span><span class="sxs-lookup"><span data-stu-id="dfdca-347">121</span></span>

[<span data-ttu-id="dfdca-348">以網路為基礎的系統管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="dfdca-349">122</span><span class="sxs-lookup"><span data-stu-id="dfdca-349">122</span></span>

[<span data-ttu-id="dfdca-350">記錄代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="dfdca-351">ADFS-角色服務 (8) </span><span class="sxs-lookup"><span data-stu-id="dfdca-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="dfdca-352">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-352">Value</span></span>

<span data-ttu-id="dfdca-353">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-353">Name</span></span>

<span data-ttu-id="dfdca-354">125</span><span class="sxs-lookup"><span data-stu-id="dfdca-354">125</span></span>

[<span data-ttu-id="dfdca-355">Active Directory 同盟服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="dfdca-356">126</span><span class="sxs-lookup"><span data-stu-id="dfdca-356">126</span></span>

[<span data-ttu-id="dfdca-357">同盟服務原則</span><span class="sxs-lookup"><span data-stu-id="dfdca-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="dfdca-358">127</span><span class="sxs-lookup"><span data-stu-id="dfdca-358">127</span></span>

[<span data-ttu-id="dfdca-359">AD FS 網頁代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="dfdca-360">128</span><span class="sxs-lookup"><span data-stu-id="dfdca-360">128</span></span>

[<span data-ttu-id="dfdca-361">宣告感知代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="dfdca-362">129</span><span class="sxs-lookup"><span data-stu-id="dfdca-362">129</span></span>

[<span data-ttu-id="dfdca-363">Windows 權杖型代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="dfdca-364">遠端桌面服務-角色服務 (18) </span><span class="sxs-lookup"><span data-stu-id="dfdca-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="dfdca-365">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-365">Value</span></span>

<span data-ttu-id="dfdca-366">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-366">Name</span></span>

<span data-ttu-id="dfdca-367">130</span><span class="sxs-lookup"><span data-stu-id="dfdca-367">130</span></span>

<span data-ttu-id="dfdca-368">遠端桌面工作階段主機</span><span class="sxs-lookup"><span data-stu-id="dfdca-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="dfdca-369">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-370">131</span><span class="sxs-lookup"><span data-stu-id="dfdca-370">131</span></span>

[<span data-ttu-id="dfdca-371">遠端桌面授權</span><span class="sxs-lookup"><span data-stu-id="dfdca-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-372">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-373">132</span><span class="sxs-lookup"><span data-stu-id="dfdca-373">132</span></span>

<span data-ttu-id="dfdca-374">遠端桌面閘道</span><span class="sxs-lookup"><span data-stu-id="dfdca-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="dfdca-375">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-376">133</span><span class="sxs-lookup"><span data-stu-id="dfdca-376">133</span></span>

<span data-ttu-id="dfdca-377">遠端桌面連線代理人</span><span class="sxs-lookup"><span data-stu-id="dfdca-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="dfdca-378">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-379">134</span><span class="sxs-lookup"><span data-stu-id="dfdca-379">134</span></span>

<span data-ttu-id="dfdca-380">遠端桌面 Web 存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="dfdca-381">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-382">322</span><span class="sxs-lookup"><span data-stu-id="dfdca-382">322</span></span>

<span data-ttu-id="dfdca-383">遠端桌面虛擬主機</span><span class="sxs-lookup"><span data-stu-id="dfdca-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="dfdca-384">遠端桌面虛擬化主機-角色服務 (322) </span><span class="sxs-lookup"><span data-stu-id="dfdca-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="dfdca-385">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-385">Value</span></span>

<span data-ttu-id="dfdca-386">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-386">Name</span></span>

<span data-ttu-id="dfdca-387">325</span><span class="sxs-lookup"><span data-stu-id="dfdca-387">325</span></span>

[<span data-ttu-id="dfdca-388">核心服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-389">327</span><span class="sxs-lookup"><span data-stu-id="dfdca-389">327</span></span>

[<span data-ttu-id="dfdca-390">遠端桌面虛擬圖形</span><span class="sxs-lookup"><span data-stu-id="dfdca-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-391">列印和檔服務-角色服務 (7) </span><span class="sxs-lookup"><span data-stu-id="dfdca-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="dfdca-392">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-392">Value</span></span>

<span data-ttu-id="dfdca-393">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-393">Name</span></span>

<span data-ttu-id="dfdca-394">135</span><span class="sxs-lookup"><span data-stu-id="dfdca-394">135</span></span>

<span data-ttu-id="dfdca-395">列印伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-395">Print Server</span></span>

<span data-ttu-id="dfdca-396">136</span><span class="sxs-lookup"><span data-stu-id="dfdca-396">136</span></span>

<span data-ttu-id="dfdca-397">網際網路列印</span><span class="sxs-lookup"><span data-stu-id="dfdca-397">Internet Printing</span></span>

<span data-ttu-id="dfdca-398">137</span><span class="sxs-lookup"><span data-stu-id="dfdca-398">137</span></span>

<span data-ttu-id="dfdca-399">LPD 列印服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-399">LPD Print Service</span></span>

<span data-ttu-id="dfdca-400">328</span><span class="sxs-lookup"><span data-stu-id="dfdca-400">328</span></span>

[<span data-ttu-id="dfdca-401">分散式掃描伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-402">Web 服務器 (IIS) -角色服務 (2) </span><span class="sxs-lookup"><span data-stu-id="dfdca-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="dfdca-403">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-403">Value</span></span>

<span data-ttu-id="dfdca-404">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-404">Name</span></span>

<span data-ttu-id="dfdca-405">140</span><span class="sxs-lookup"><span data-stu-id="dfdca-405">140</span></span>

<span data-ttu-id="dfdca-406">Web 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-406">Web Server</span></span>

<span data-ttu-id="dfdca-407">141</span><span class="sxs-lookup"><span data-stu-id="dfdca-407">141</span></span>

<span data-ttu-id="dfdca-408">一般 HTTP 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-408">Common HTTP Features</span></span>

<span data-ttu-id="dfdca-409">142</span><span class="sxs-lookup"><span data-stu-id="dfdca-409">142</span></span>

<span data-ttu-id="dfdca-410">靜態內容</span><span class="sxs-lookup"><span data-stu-id="dfdca-410">Static Content</span></span>

<span data-ttu-id="dfdca-411">143</span><span class="sxs-lookup"><span data-stu-id="dfdca-411">143</span></span>

<span data-ttu-id="dfdca-412">預設文件</span><span class="sxs-lookup"><span data-stu-id="dfdca-412">Default Document</span></span>

<span data-ttu-id="dfdca-413">144</span><span class="sxs-lookup"><span data-stu-id="dfdca-413">144</span></span>

<span data-ttu-id="dfdca-414">瀏覽目錄</span><span class="sxs-lookup"><span data-stu-id="dfdca-414">Directory Browse</span></span>

<span data-ttu-id="dfdca-415">145</span><span class="sxs-lookup"><span data-stu-id="dfdca-415">145</span></span>

<span data-ttu-id="dfdca-416">HTTP 錯誤</span><span class="sxs-lookup"><span data-stu-id="dfdca-416">HTTP Errors</span></span>

<span data-ttu-id="dfdca-417">146</span><span class="sxs-lookup"><span data-stu-id="dfdca-417">146</span></span>

<span data-ttu-id="dfdca-418">HTTP 重新導向</span><span class="sxs-lookup"><span data-stu-id="dfdca-418">HTTP Redirection</span></span>

<span data-ttu-id="dfdca-419">147</span><span class="sxs-lookup"><span data-stu-id="dfdca-419">147</span></span>

<span data-ttu-id="dfdca-420">應用程式開發</span><span class="sxs-lookup"><span data-stu-id="dfdca-420">Application Development</span></span>

<span data-ttu-id="dfdca-421">148</span><span class="sxs-lookup"><span data-stu-id="dfdca-421">148</span></span>

<span data-ttu-id="dfdca-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="dfdca-422">ASP.NET</span></span>

<span data-ttu-id="dfdca-423">149</span><span class="sxs-lookup"><span data-stu-id="dfdca-423">149</span></span>

<span data-ttu-id="dfdca-424">.NET 擴充性</span><span class="sxs-lookup"><span data-stu-id="dfdca-424">.NET Extensibility</span></span>

<span data-ttu-id="dfdca-425">150</span><span class="sxs-lookup"><span data-stu-id="dfdca-425">150</span></span>

<span data-ttu-id="dfdca-426">ASP</span><span class="sxs-lookup"><span data-stu-id="dfdca-426">ASP</span></span>

<span data-ttu-id="dfdca-427">151</span><span class="sxs-lookup"><span data-stu-id="dfdca-427">151</span></span>

<span data-ttu-id="dfdca-428">CGI</span><span class="sxs-lookup"><span data-stu-id="dfdca-428">CGI</span></span>

<span data-ttu-id="dfdca-429">152</span><span class="sxs-lookup"><span data-stu-id="dfdca-429">152</span></span>

<span data-ttu-id="dfdca-430">ISAPI 擴充程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-430">ISAPI Extensions</span></span>

<span data-ttu-id="dfdca-431">153</span><span class="sxs-lookup"><span data-stu-id="dfdca-431">153</span></span>

<span data-ttu-id="dfdca-432">ISAPI 篩選</span><span class="sxs-lookup"><span data-stu-id="dfdca-432">ISAPI Filters</span></span>

<span data-ttu-id="dfdca-433">154</span><span class="sxs-lookup"><span data-stu-id="dfdca-433">154</span></span>

<span data-ttu-id="dfdca-434">伺服器端包含</span><span class="sxs-lookup"><span data-stu-id="dfdca-434">Server Side Includes</span></span>

<span data-ttu-id="dfdca-435">155</span><span class="sxs-lookup"><span data-stu-id="dfdca-435">155</span></span>

<span data-ttu-id="dfdca-436">健康情況和診斷</span><span class="sxs-lookup"><span data-stu-id="dfdca-436">Health And Diagnostics</span></span>

<span data-ttu-id="dfdca-437">156</span><span class="sxs-lookup"><span data-stu-id="dfdca-437">156</span></span>

<span data-ttu-id="dfdca-438">HTTP 記錄</span><span class="sxs-lookup"><span data-stu-id="dfdca-438">HTTP Logging</span></span>

<span data-ttu-id="dfdca-439">157</span><span class="sxs-lookup"><span data-stu-id="dfdca-439">157</span></span>

<span data-ttu-id="dfdca-440">記錄工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-440">Logging Tools</span></span>

<span data-ttu-id="dfdca-441">158</span><span class="sxs-lookup"><span data-stu-id="dfdca-441">158</span></span>

<span data-ttu-id="dfdca-442">要求監視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-442">Request Monitor</span></span>

<span data-ttu-id="dfdca-443">159</span><span class="sxs-lookup"><span data-stu-id="dfdca-443">159</span></span>

<span data-ttu-id="dfdca-444">追蹤</span><span class="sxs-lookup"><span data-stu-id="dfdca-444">Tracing</span></span>

<span data-ttu-id="dfdca-445">160</span><span class="sxs-lookup"><span data-stu-id="dfdca-445">160</span></span>

<span data-ttu-id="dfdca-446">自訂記錄</span><span class="sxs-lookup"><span data-stu-id="dfdca-446">Custom Logging</span></span>

<span data-ttu-id="dfdca-447">161</span><span class="sxs-lookup"><span data-stu-id="dfdca-447">161</span></span>

<span data-ttu-id="dfdca-448">ODBC 記錄</span><span class="sxs-lookup"><span data-stu-id="dfdca-448">ODBC Logging</span></span>

<span data-ttu-id="dfdca-449">162</span><span class="sxs-lookup"><span data-stu-id="dfdca-449">162</span></span>

<span data-ttu-id="dfdca-450">安全性</span><span class="sxs-lookup"><span data-stu-id="dfdca-450">Security</span></span>

<span data-ttu-id="dfdca-451">163</span><span class="sxs-lookup"><span data-stu-id="dfdca-451">163</span></span>

<span data-ttu-id="dfdca-452">基本驗證</span><span class="sxs-lookup"><span data-stu-id="dfdca-452">Basic Authentication</span></span>

<span data-ttu-id="dfdca-453">164</span><span class="sxs-lookup"><span data-stu-id="dfdca-453">164</span></span>

<span data-ttu-id="dfdca-454">Windows 驗證</span><span class="sxs-lookup"><span data-stu-id="dfdca-454">Windows Authentication</span></span>

<span data-ttu-id="dfdca-455">165</span><span class="sxs-lookup"><span data-stu-id="dfdca-455">165</span></span>

<span data-ttu-id="dfdca-456">摘要式驗證</span><span class="sxs-lookup"><span data-stu-id="dfdca-456">Digest Authentication</span></span>

<span data-ttu-id="dfdca-457">166</span><span class="sxs-lookup"><span data-stu-id="dfdca-457">166</span></span>

<span data-ttu-id="dfdca-458">用戶端憑證對應驗證</span><span class="sxs-lookup"><span data-stu-id="dfdca-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="dfdca-459">167</span><span class="sxs-lookup"><span data-stu-id="dfdca-459">167</span></span>

<span data-ttu-id="dfdca-460">IIS 用戶端憑證對應驗證</span><span class="sxs-lookup"><span data-stu-id="dfdca-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="dfdca-461">168</span><span class="sxs-lookup"><span data-stu-id="dfdca-461">168</span></span>

<span data-ttu-id="dfdca-462">URL 授權</span><span class="sxs-lookup"><span data-stu-id="dfdca-462">URL Authorization</span></span>

<span data-ttu-id="dfdca-463">169</span><span class="sxs-lookup"><span data-stu-id="dfdca-463">169</span></span>

<span data-ttu-id="dfdca-464">要求篩選</span><span class="sxs-lookup"><span data-stu-id="dfdca-464">Request Filtering</span></span>

<span data-ttu-id="dfdca-465">170</span><span class="sxs-lookup"><span data-stu-id="dfdca-465">170</span></span>

<span data-ttu-id="dfdca-466">IP 和網域限制</span><span class="sxs-lookup"><span data-stu-id="dfdca-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="dfdca-467">171</span><span class="sxs-lookup"><span data-stu-id="dfdca-467">171</span></span>

<span data-ttu-id="dfdca-468">效能</span><span class="sxs-lookup"><span data-stu-id="dfdca-468">Performance</span></span>

<span data-ttu-id="dfdca-469">172</span><span class="sxs-lookup"><span data-stu-id="dfdca-469">172</span></span>

<span data-ttu-id="dfdca-470">靜態內容壓縮</span><span class="sxs-lookup"><span data-stu-id="dfdca-470">Static Content Compression</span></span>

<span data-ttu-id="dfdca-471">173</span><span class="sxs-lookup"><span data-stu-id="dfdca-471">173</span></span>

<span data-ttu-id="dfdca-472">動態內容壓縮</span><span class="sxs-lookup"><span data-stu-id="dfdca-472">Dynamic Content Compression</span></span>

<span data-ttu-id="dfdca-473">174</span><span class="sxs-lookup"><span data-stu-id="dfdca-473">174</span></span>

<span data-ttu-id="dfdca-474">管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-474">Management Tools</span></span>

<span data-ttu-id="dfdca-475">175</span><span class="sxs-lookup"><span data-stu-id="dfdca-475">175</span></span>

<span data-ttu-id="dfdca-476">IIS 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-476">IIS Management Console</span></span>

<span data-ttu-id="dfdca-477">176</span><span class="sxs-lookup"><span data-stu-id="dfdca-477">176</span></span>

<span data-ttu-id="dfdca-478">IIS 管理腳本和工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="dfdca-479">177</span><span class="sxs-lookup"><span data-stu-id="dfdca-479">177</span></span>

<span data-ttu-id="dfdca-480">Management Service</span><span class="sxs-lookup"><span data-stu-id="dfdca-480">Management Service</span></span>

<span data-ttu-id="dfdca-481">178</span><span class="sxs-lookup"><span data-stu-id="dfdca-481">178</span></span>

<span data-ttu-id="dfdca-482">IIS 6 管理相容性</span><span class="sxs-lookup"><span data-stu-id="dfdca-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="dfdca-483">179</span><span class="sxs-lookup"><span data-stu-id="dfdca-483">179</span></span>

<span data-ttu-id="dfdca-484">IIS 6 Metabase 相容性</span><span class="sxs-lookup"><span data-stu-id="dfdca-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="dfdca-485">180</span><span class="sxs-lookup"><span data-stu-id="dfdca-485">180</span></span>

<span data-ttu-id="dfdca-486">IIS 6 WMI 相容性</span><span class="sxs-lookup"><span data-stu-id="dfdca-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="dfdca-487">181</span><span class="sxs-lookup"><span data-stu-id="dfdca-487">181</span></span>

<span data-ttu-id="dfdca-488">IIS 6 指令碼工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="dfdca-489">182</span><span class="sxs-lookup"><span data-stu-id="dfdca-489">182</span></span>

<span data-ttu-id="dfdca-490">IIS 6 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-490">IIS 6 Management Console</span></span>

<span data-ttu-id="dfdca-491">183</span><span class="sxs-lookup"><span data-stu-id="dfdca-491">183</span></span>

<span data-ttu-id="dfdca-492">FTP 發行服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="dfdca-493">184</span><span class="sxs-lookup"><span data-stu-id="dfdca-493">184</span></span>

<span data-ttu-id="dfdca-494">FTP 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-494">FTP Server</span></span>

<span data-ttu-id="dfdca-495">185</span><span class="sxs-lookup"><span data-stu-id="dfdca-495">185</span></span>

<span data-ttu-id="dfdca-496">FTP 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-496">FTP Management Console</span></span><br/>

<span data-ttu-id="dfdca-497">314</span><span class="sxs-lookup"><span data-stu-id="dfdca-497">314</span></span>

<span data-ttu-id="dfdca-498">WebDAV 發行</span><span class="sxs-lookup"><span data-stu-id="dfdca-498">WebDAV Publishing</span></span>

<span data-ttu-id="dfdca-499">316</span><span class="sxs-lookup"><span data-stu-id="dfdca-499">316</span></span>

<span data-ttu-id="dfdca-500">FTP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-500">FTP Service</span></span><br/>

<span data-ttu-id="dfdca-501">317</span><span class="sxs-lookup"><span data-stu-id="dfdca-501">317</span></span>

<span data-ttu-id="dfdca-502">FTP 擴充性</span><span class="sxs-lookup"><span data-stu-id="dfdca-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="dfdca-503">336</span><span class="sxs-lookup"><span data-stu-id="dfdca-503">336</span></span>

<span data-ttu-id="dfdca-504">可裝載 IIS 的 Web 核心</span><span class="sxs-lookup"><span data-stu-id="dfdca-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="dfdca-505">413</span><span class="sxs-lookup"><span data-stu-id="dfdca-505">413</span></span>

[<span data-ttu-id="dfdca-506">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="dfdca-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="dfdca-507">414</span><span class="sxs-lookup"><span data-stu-id="dfdca-507">414</span></span>

[<span data-ttu-id="dfdca-508">.NET 擴充性 4.5</span><span class="sxs-lookup"><span data-stu-id="dfdca-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="dfdca-509">445</span><span class="sxs-lookup"><span data-stu-id="dfdca-509">445</span></span>

[<span data-ttu-id="dfdca-510">appialization</span><span class="sxs-lookup"><span data-stu-id="dfdca-510">appialization</span></span>](/windows)

<span data-ttu-id="dfdca-511">446</span><span class="sxs-lookup"><span data-stu-id="dfdca-511">446</span></span>

[<span data-ttu-id="dfdca-512">集中式 SSL 憑證支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="dfdca-513">447</span><span class="sxs-lookup"><span data-stu-id="dfdca-513">447</span></span>

[<span data-ttu-id="dfdca-514">WebSocket 通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="dfdca-515">訊息佇列-功能 (49) </span><span class="sxs-lookup"><span data-stu-id="dfdca-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="dfdca-516">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-516">Value</span></span>

<span data-ttu-id="dfdca-517">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-517">Name</span></span>

<span data-ttu-id="dfdca-518">190</span><span class="sxs-lookup"><span data-stu-id="dfdca-518">190</span></span>

<span data-ttu-id="dfdca-519">訊息佇列服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-519">Message Queuing Services</span></span>

<span data-ttu-id="dfdca-520">191</span><span class="sxs-lookup"><span data-stu-id="dfdca-520">191</span></span>

<span data-ttu-id="dfdca-521">訊息佇列伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-521">Message Queuing Server</span></span>

<span data-ttu-id="dfdca-522">192</span><span class="sxs-lookup"><span data-stu-id="dfdca-522">192</span></span>

<span data-ttu-id="dfdca-523">目錄服務整合</span><span class="sxs-lookup"><span data-stu-id="dfdca-523">Directory Service Integration</span></span>

<span data-ttu-id="dfdca-524">193</span><span class="sxs-lookup"><span data-stu-id="dfdca-524">193</span></span>

<span data-ttu-id="dfdca-525">訊息佇列觸發程序</span><span class="sxs-lookup"><span data-stu-id="dfdca-525">Message Queuing Triggers</span></span>

<span data-ttu-id="dfdca-526">194</span><span class="sxs-lookup"><span data-stu-id="dfdca-526">194</span></span>

<span data-ttu-id="dfdca-527">HTTP 支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-527">HTTP Support</span></span>

<span data-ttu-id="dfdca-528">195</span><span class="sxs-lookup"><span data-stu-id="dfdca-528">195</span></span>

<span data-ttu-id="dfdca-529">路由服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-529">Routing Service</span></span>

<span data-ttu-id="dfdca-530">196</span><span class="sxs-lookup"><span data-stu-id="dfdca-530">196</span></span>

[<span data-ttu-id="dfdca-531">Windows 2000 用戶端支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-532">197</span><span class="sxs-lookup"><span data-stu-id="dfdca-532">197</span></span>

<span data-ttu-id="dfdca-533">訊息佇列 DCOM Proxy</span><span class="sxs-lookup"><span data-stu-id="dfdca-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="dfdca-534">228</span><span class="sxs-lookup"><span data-stu-id="dfdca-534">228</span></span>

<span data-ttu-id="dfdca-535">多點傳送支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-535">Multicasting Support</span></span>

<span data-ttu-id="dfdca-536">Active Directory 憑證服務-角色服務 (16) </span><span class="sxs-lookup"><span data-stu-id="dfdca-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="dfdca-537">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-537">Value</span></span>

<span data-ttu-id="dfdca-538">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-538">Name</span></span>

<span data-ttu-id="dfdca-539">200</span><span class="sxs-lookup"><span data-stu-id="dfdca-539">200</span></span>

<span data-ttu-id="dfdca-540">憑證授權單位</span><span class="sxs-lookup"><span data-stu-id="dfdca-540">Certification Authority</span></span>

<span data-ttu-id="dfdca-541">201</span><span class="sxs-lookup"><span data-stu-id="dfdca-541">201</span></span>

<span data-ttu-id="dfdca-542">憑證授權單位網頁註冊。</span><span class="sxs-lookup"><span data-stu-id="dfdca-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="dfdca-543">202</span><span class="sxs-lookup"><span data-stu-id="dfdca-543">202</span></span>

<span data-ttu-id="dfdca-544">線上回應</span><span class="sxs-lookup"><span data-stu-id="dfdca-544">Online Responder</span></span>

<span data-ttu-id="dfdca-545">204</span><span class="sxs-lookup"><span data-stu-id="dfdca-545">204</span></span>

<span data-ttu-id="dfdca-546">網路裝置註冊服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="dfdca-547">318</span><span class="sxs-lookup"><span data-stu-id="dfdca-547">318</span></span>

[<span data-ttu-id="dfdca-548">憑證註冊 Web 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-549">319</span><span class="sxs-lookup"><span data-stu-id="dfdca-549">319</span></span>

[<span data-ttu-id="dfdca-550">憑證註冊原則 Web 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-551">網路原則與存取服務-角色服務 (14) </span><span class="sxs-lookup"><span data-stu-id="dfdca-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="dfdca-552">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-552">Value</span></span>

<span data-ttu-id="dfdca-553">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-553">Name</span></span>

<span data-ttu-id="dfdca-554">205</span><span class="sxs-lookup"><span data-stu-id="dfdca-554">205</span></span>

[<span data-ttu-id="dfdca-555">網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="dfdca-556">206</span><span class="sxs-lookup"><span data-stu-id="dfdca-556">206</span></span>

[<span data-ttu-id="dfdca-557">VPN</span><span class="sxs-lookup"><span data-stu-id="dfdca-557">VPN</span></span>](#vpn)

<span data-ttu-id="dfdca-558">207</span><span class="sxs-lookup"><span data-stu-id="dfdca-558">207</span></span>

[<span data-ttu-id="dfdca-559">遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="dfdca-560">208</span><span class="sxs-lookup"><span data-stu-id="dfdca-560">208</span></span>

[<span data-ttu-id="dfdca-561">路由</span><span class="sxs-lookup"><span data-stu-id="dfdca-561">Routing</span></span>](#routing)

<span data-ttu-id="dfdca-562">210</span><span class="sxs-lookup"><span data-stu-id="dfdca-562">210</span></span>

[<span data-ttu-id="dfdca-563">健康情況登錄授權單位</span><span class="sxs-lookup"><span data-stu-id="dfdca-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="dfdca-564">250</span><span class="sxs-lookup"><span data-stu-id="dfdca-564">250</span></span>

[<span data-ttu-id="dfdca-565">主機認證授權通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="dfdca-566">UDDI 服務-角色服務 (11) </span><span class="sxs-lookup"><span data-stu-id="dfdca-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="dfdca-567">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-567">Value</span></span>

<span data-ttu-id="dfdca-568">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-568">Name</span></span>

<span data-ttu-id="dfdca-569">215</span><span class="sxs-lookup"><span data-stu-id="dfdca-569">215</span></span>

[<span data-ttu-id="dfdca-570">UDDI 服務 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-571">216</span><span class="sxs-lookup"><span data-stu-id="dfdca-571">216</span></span>

[<span data-ttu-id="dfdca-572">UDDI 服務資料庫</span><span class="sxs-lookup"><span data-stu-id="dfdca-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-573">Windows 處理常式啟用服務-角色服務 (41) </span><span class="sxs-lookup"><span data-stu-id="dfdca-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="dfdca-574">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-574">Value</span></span>

<span data-ttu-id="dfdca-575">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-575">Name</span></span>

<span data-ttu-id="dfdca-576">217</span><span class="sxs-lookup"><span data-stu-id="dfdca-576">217</span></span>

<span data-ttu-id="dfdca-577">設定 API</span><span class="sxs-lookup"><span data-stu-id="dfdca-577">Configuration API</span></span>

<span data-ttu-id="dfdca-578">218</span><span class="sxs-lookup"><span data-stu-id="dfdca-578">218</span></span>

<span data-ttu-id="dfdca-579">.NET 環境</span><span class="sxs-lookup"><span data-stu-id="dfdca-579">.NET Environment</span></span>

<span data-ttu-id="dfdca-580">219</span><span class="sxs-lookup"><span data-stu-id="dfdca-580">219</span></span>

<span data-ttu-id="dfdca-581">處理序模型</span><span class="sxs-lookup"><span data-stu-id="dfdca-581">Process Model</span></span>

<span data-ttu-id="dfdca-582">.NET Framework 3.5.1-功能 (36) </span><span class="sxs-lookup"><span data-stu-id="dfdca-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="dfdca-583">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-583">Value</span></span>

<span data-ttu-id="dfdca-584">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-584">Name</span></span>

<span data-ttu-id="dfdca-585">220</span><span class="sxs-lookup"><span data-stu-id="dfdca-585">220</span></span>

<span data-ttu-id="dfdca-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="dfdca-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="dfdca-587">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-588">221</span><span class="sxs-lookup"><span data-stu-id="dfdca-588">221</span></span>

<span data-ttu-id="dfdca-589">WCF 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-589">WCF Activation</span></span>

<span data-ttu-id="dfdca-590">222</span><span class="sxs-lookup"><span data-stu-id="dfdca-590">222</span></span>

<span data-ttu-id="dfdca-591">HTTP 啟動</span><span class="sxs-lookup"><span data-stu-id="dfdca-591">HTTP Activation</span></span>

<span data-ttu-id="dfdca-592">223</span><span class="sxs-lookup"><span data-stu-id="dfdca-592">223</span></span>

<span data-ttu-id="dfdca-593">非 HTTP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-593">Non-HTTP Activation</span></span>

<span data-ttu-id="dfdca-594">227</span><span class="sxs-lookup"><span data-stu-id="dfdca-594">227</span></span>

<span data-ttu-id="dfdca-595">XPS 檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-595">XPS Viewer</span></span><br/>

<span data-ttu-id="dfdca-596">SNMP 服務-功能 (59) </span><span class="sxs-lookup"><span data-stu-id="dfdca-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="dfdca-597">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-597">Value</span></span>

<span data-ttu-id="dfdca-598">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-598">Name</span></span>

<span data-ttu-id="dfdca-599">224</span><span class="sxs-lookup"><span data-stu-id="dfdca-599">224</span></span>

[<span data-ttu-id="dfdca-600">SNMP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="dfdca-601">225</span><span class="sxs-lookup"><span data-stu-id="dfdca-601">225</span></span>

[<span data-ttu-id="dfdca-602">SNMP WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="dfdca-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="dfdca-603">應用程式服務-角色服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-603">Application Services - Role Services</span></span>

<span data-ttu-id="dfdca-604">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-604">Value</span></span>

<span data-ttu-id="dfdca-605">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-605">Name</span></span>

<span data-ttu-id="dfdca-606">230</span><span class="sxs-lookup"><span data-stu-id="dfdca-606">230</span></span>

[<span data-ttu-id="dfdca-607">.NET Framework 3.5。1</span><span class="sxs-lookup"><span data-stu-id="dfdca-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-608">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-609">231</span><span class="sxs-lookup"><span data-stu-id="dfdca-609">231</span></span>

[<span data-ttu-id="dfdca-610">網頁伺服器 (IIS) 支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="dfdca-611">232</span><span class="sxs-lookup"><span data-stu-id="dfdca-611">232</span></span>

[<span data-ttu-id="dfdca-612">COM + 網路存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="dfdca-613">233</span><span class="sxs-lookup"><span data-stu-id="dfdca-613">233</span></span>

[<span data-ttu-id="dfdca-614">TCP 連接埠共用</span><span class="sxs-lookup"><span data-stu-id="dfdca-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="dfdca-615">234</span><span class="sxs-lookup"><span data-stu-id="dfdca-615">234</span></span>

[<span data-ttu-id="dfdca-616">Windows 處理程序啟動服務支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="dfdca-617">235</span><span class="sxs-lookup"><span data-stu-id="dfdca-617">235</span></span>

[<span data-ttu-id="dfdca-618">HTTP 啟動</span><span class="sxs-lookup"><span data-stu-id="dfdca-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="dfdca-619">236</span><span class="sxs-lookup"><span data-stu-id="dfdca-619">236</span></span>

[<span data-ttu-id="dfdca-620">訊息佇列啟動</span><span class="sxs-lookup"><span data-stu-id="dfdca-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="dfdca-621">237</span><span class="sxs-lookup"><span data-stu-id="dfdca-621">237</span></span>

[<span data-ttu-id="dfdca-622">TCP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="dfdca-623">238</span><span class="sxs-lookup"><span data-stu-id="dfdca-623">238</span></span>

[<span data-ttu-id="dfdca-624">具名管道啟動</span><span class="sxs-lookup"><span data-stu-id="dfdca-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="dfdca-625">239</span><span class="sxs-lookup"><span data-stu-id="dfdca-625">239</span></span>

[<span data-ttu-id="dfdca-626">分散式交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="dfdca-627">240</span><span class="sxs-lookup"><span data-stu-id="dfdca-627">240</span></span>

[<span data-ttu-id="dfdca-628">傳入遠端交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="dfdca-629">241</span><span class="sxs-lookup"><span data-stu-id="dfdca-629">241</span></span>

[<span data-ttu-id="dfdca-630">連出遠端交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="dfdca-631">242</span><span class="sxs-lookup"><span data-stu-id="dfdca-631">242</span></span>

[<span data-ttu-id="dfdca-632">WS-自動交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="dfdca-633">353</span><span class="sxs-lookup"><span data-stu-id="dfdca-633">353</span></span>

[<span data-ttu-id="dfdca-634">適用于 .NET 4.0 的應用程式伺服器擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-635">Windows 部署服務-Role (19) </span><span class="sxs-lookup"><span data-stu-id="dfdca-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="dfdca-636">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-636">Value</span></span>

<span data-ttu-id="dfdca-637">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-637">Name</span></span>

<span data-ttu-id="dfdca-638">251</span><span class="sxs-lookup"><span data-stu-id="dfdca-638">251</span></span>

<span data-ttu-id="dfdca-639">部署伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-639">Deployment Server</span></span>

<span data-ttu-id="dfdca-640">252</span><span class="sxs-lookup"><span data-stu-id="dfdca-640">252</span></span>

<span data-ttu-id="dfdca-641">傳輸伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-641">Transport Server</span></span>

<span data-ttu-id="dfdca-642">Active Directory Rights Management Services-角色服務 (17) </span><span class="sxs-lookup"><span data-stu-id="dfdca-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="dfdca-643">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-643">Value</span></span>

<span data-ttu-id="dfdca-644">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-644">Name</span></span>

<span data-ttu-id="dfdca-645">253</span><span class="sxs-lookup"><span data-stu-id="dfdca-645">253</span></span>

<span data-ttu-id="dfdca-646">Active Directory Rights Management Server</span><span class="sxs-lookup"><span data-stu-id="dfdca-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="dfdca-647">254</span><span class="sxs-lookup"><span data-stu-id="dfdca-647">254</span></span>

<span data-ttu-id="dfdca-648">識別身分同盟支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-648">Identity Federation Support</span></span>

<span data-ttu-id="dfdca-649">遠端伺服器管理工具 (67) </span><span class="sxs-lookup"><span data-stu-id="dfdca-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="dfdca-650">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-650">Value</span></span>

<span data-ttu-id="dfdca-651">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-651">Name</span></span>

<span data-ttu-id="dfdca-652">256</span><span class="sxs-lookup"><span data-stu-id="dfdca-652">256</span></span>

[<span data-ttu-id="dfdca-653">角色管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="dfdca-654">257</span><span class="sxs-lookup"><span data-stu-id="dfdca-654">257</span></span>

[<span data-ttu-id="dfdca-655">AD DS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-656">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-657">258</span><span class="sxs-lookup"><span data-stu-id="dfdca-657">258</span></span>

[<span data-ttu-id="dfdca-658">AD LDS Snap-Ins 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-659">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-660">259</span><span class="sxs-lookup"><span data-stu-id="dfdca-660">259</span></span>

<span data-ttu-id="dfdca-661">Active Directory 憑證服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="dfdca-662">260</span><span class="sxs-lookup"><span data-stu-id="dfdca-662">260</span></span>

[<span data-ttu-id="dfdca-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="dfdca-664">261</span><span class="sxs-lookup"><span data-stu-id="dfdca-664">261</span></span>

<span data-ttu-id="dfdca-665">列印和檔服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="dfdca-666">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-667">262</span><span class="sxs-lookup"><span data-stu-id="dfdca-667">262</span></span>

[<span data-ttu-id="dfdca-668">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="dfdca-669">263</span><span class="sxs-lookup"><span data-stu-id="dfdca-669">263</span></span>

[<span data-ttu-id="dfdca-670">遠端桌面服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-671">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-672">264</span><span class="sxs-lookup"><span data-stu-id="dfdca-672">264</span></span>

<span data-ttu-id="dfdca-673">Windows 部署服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="dfdca-674">265</span><span class="sxs-lookup"><span data-stu-id="dfdca-674">265</span></span>

[<span data-ttu-id="dfdca-675">功能管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="dfdca-676">266</span><span class="sxs-lookup"><span data-stu-id="dfdca-676">266</span></span>

<span data-ttu-id="dfdca-677">BitLocker 磁碟機加密工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="dfdca-678">267</span><span class="sxs-lookup"><span data-stu-id="dfdca-678">267</span></span>

<span data-ttu-id="dfdca-679">BITS 伺服器擴充功能工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="dfdca-680">268</span><span class="sxs-lookup"><span data-stu-id="dfdca-680">268</span></span>

[<span data-ttu-id="dfdca-681">容錯移轉叢集工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="dfdca-682">269</span><span class="sxs-lookup"><span data-stu-id="dfdca-682">269</span></span>

<span data-ttu-id="dfdca-683">網路負載平衡工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="dfdca-684">270</span><span class="sxs-lookup"><span data-stu-id="dfdca-684">270</span></span>

<span data-ttu-id="dfdca-685">SMTP 伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-685">SMTP Server Tools</span></span>

<span data-ttu-id="dfdca-686">273</span><span class="sxs-lookup"><span data-stu-id="dfdca-686">273</span></span>

[<span data-ttu-id="dfdca-687">DNS 伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="dfdca-688">277</span><span class="sxs-lookup"><span data-stu-id="dfdca-688">277</span></span>

<span data-ttu-id="dfdca-689">檔案服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-689">File Services Tools</span></span>

<span data-ttu-id="dfdca-690">278</span><span class="sxs-lookup"><span data-stu-id="dfdca-690">278</span></span>

<span data-ttu-id="dfdca-691">分散式檔案系統工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-691">Distributed File System Tools</span></span>

<span data-ttu-id="dfdca-692">279</span><span class="sxs-lookup"><span data-stu-id="dfdca-692">279</span></span>

<span data-ttu-id="dfdca-693">檔案伺服器 Resource Manager 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="dfdca-694">280</span><span class="sxs-lookup"><span data-stu-id="dfdca-694">280</span></span>

[<span data-ttu-id="dfdca-695">Services For Network File System 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="dfdca-696">281</span><span class="sxs-lookup"><span data-stu-id="dfdca-696">281</span></span>

<span data-ttu-id="dfdca-697">Web 服務器 (IIS) 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="dfdca-698">284</span><span class="sxs-lookup"><span data-stu-id="dfdca-698">284</span></span>

[<span data-ttu-id="dfdca-699">遠端桌面工作階段主機工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-700">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-701">285</span><span class="sxs-lookup"><span data-stu-id="dfdca-701">285</span></span>

<span data-ttu-id="dfdca-702">遠端桌面閘道工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="dfdca-703">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-704">286</span><span class="sxs-lookup"><span data-stu-id="dfdca-704">286</span></span>

<span data-ttu-id="dfdca-705">遠端桌面授權工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="dfdca-706">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-707">288</span><span class="sxs-lookup"><span data-stu-id="dfdca-707">288</span></span>

<span data-ttu-id="dfdca-708">傳真伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-708">Fax Server Tools</span></span>

<span data-ttu-id="dfdca-709">290</span><span class="sxs-lookup"><span data-stu-id="dfdca-709">290</span></span>

<span data-ttu-id="dfdca-710">WINS 伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-710">WINS Server Tools</span></span>

<span data-ttu-id="dfdca-711">291</span><span class="sxs-lookup"><span data-stu-id="dfdca-711">291</span></span>

[<span data-ttu-id="dfdca-712">UDDI 服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-713">292</span><span class="sxs-lookup"><span data-stu-id="dfdca-713">292</span></span>

<span data-ttu-id="dfdca-714">憑證授權單位單位工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-714">Certification Authority Tools</span></span>

<span data-ttu-id="dfdca-715">293</span><span class="sxs-lookup"><span data-stu-id="dfdca-715">293</span></span>

<span data-ttu-id="dfdca-716">線上回應工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-716">Online Responder Tools</span></span>

<span data-ttu-id="dfdca-717">297</span><span class="sxs-lookup"><span data-stu-id="dfdca-717">297</span></span>

[<span data-ttu-id="dfdca-718">Server for NIS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="dfdca-719">299</span><span class="sxs-lookup"><span data-stu-id="dfdca-719">299</span></span>

[<span data-ttu-id="dfdca-720">AD DS Snap-Ins 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="dfdca-721">名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-722">300</span><span class="sxs-lookup"><span data-stu-id="dfdca-722">300</span></span>

[<span data-ttu-id="dfdca-723"> Active Directory 管理中心</span><span class="sxs-lookup"><span data-stu-id="dfdca-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="dfdca-724">301</span><span class="sxs-lookup"><span data-stu-id="dfdca-724">301</span></span>

<span data-ttu-id="dfdca-725">Hyper-v 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-725">Hyper-V Tools</span></span>

<span data-ttu-id="dfdca-726">323</span><span class="sxs-lookup"><span data-stu-id="dfdca-726">323</span></span>

[<span data-ttu-id="dfdca-727">BitLocker 修復密碼檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-728">326</span><span class="sxs-lookup"><span data-stu-id="dfdca-728">326</span></span>

[<span data-ttu-id="dfdca-729">BitLocker 磁碟機加密管理公用程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-730">329</span><span class="sxs-lookup"><span data-stu-id="dfdca-730">329</span></span>

[<span data-ttu-id="dfdca-731">AD DS 和 AD LDS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-732">330</span><span class="sxs-lookup"><span data-stu-id="dfdca-732">330</span></span>

<span data-ttu-id="dfdca-733">Active Directory 管理中心</span><span class="sxs-lookup"><span data-stu-id="dfdca-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="dfdca-734">331</span><span class="sxs-lookup"><span data-stu-id="dfdca-734">331</span></span>

[<span data-ttu-id="dfdca-735">適用於 Windows PowerShell 的 Active Directory 模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-736">337</span><span class="sxs-lookup"><span data-stu-id="dfdca-736">337</span></span>

[<span data-ttu-id="dfdca-737">遠端桌面連線代理人工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-738">410</span><span class="sxs-lookup"><span data-stu-id="dfdca-738">410</span></span>

[<span data-ttu-id="dfdca-739">IP 位址管理 (IPAM) 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="dfdca-740">450</span><span class="sxs-lookup"><span data-stu-id="dfdca-740">450</span></span>

[<span data-ttu-id="dfdca-741">Windows PowerShell 的 Hyper-V 模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="dfdca-742">462</span><span class="sxs-lookup"><span data-stu-id="dfdca-742">462</span></span>

[<span data-ttu-id="dfdca-743">Active Directory Rights Management Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="dfdca-744">465</span><span class="sxs-lookup"><span data-stu-id="dfdca-744">465</span></span>

[<span data-ttu-id="dfdca-745">共用與存放管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="dfdca-746">471</span><span class="sxs-lookup"><span data-stu-id="dfdca-746">471</span></span>

[<span data-ttu-id="dfdca-747">遠端存取管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="dfdca-748">472</span><span class="sxs-lookup"><span data-stu-id="dfdca-748">472</span></span>

[<span data-ttu-id="dfdca-749">適用於 Windows PowerShell 的遠端存取模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="dfdca-750">473</span><span class="sxs-lookup"><span data-stu-id="dfdca-750">473</span></span>

[<span data-ttu-id="dfdca-751">遠端存取 GUI 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="dfdca-752">474</span><span class="sxs-lookup"><span data-stu-id="dfdca-752">474</span></span>

[<span data-ttu-id="dfdca-753">Windows Server Update Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="dfdca-754">476</span><span class="sxs-lookup"><span data-stu-id="dfdca-754">476</span></span>

[<span data-ttu-id="dfdca-755">遠端桌面授權診斷程式工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="dfdca-756">479</span><span class="sxs-lookup"><span data-stu-id="dfdca-756">479</span></span>

[<span data-ttu-id="dfdca-757">SNMP 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="dfdca-758">480</span><span class="sxs-lookup"><span data-stu-id="dfdca-758">480</span></span>

[<span data-ttu-id="dfdca-759">大量啟用工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="dfdca-760">Windows Server Backup-功能 (39) </span><span class="sxs-lookup"><span data-stu-id="dfdca-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="dfdca-761">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-761">Value</span></span>

<span data-ttu-id="dfdca-762">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-762">Name</span></span>

<span data-ttu-id="dfdca-763">296</span><span class="sxs-lookup"><span data-stu-id="dfdca-763">296</span></span>

[<span data-ttu-id="dfdca-764">Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="dfdca-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="dfdca-765">297</span><span class="sxs-lookup"><span data-stu-id="dfdca-765">297</span></span>

[<span data-ttu-id="dfdca-766">命令列工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="dfdca-767">筆跡和手寫服務-功能 (310) </span><span class="sxs-lookup"><span data-stu-id="dfdca-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="dfdca-768">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-768">Value</span></span>

<span data-ttu-id="dfdca-769">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-769">Name</span></span>

<span data-ttu-id="dfdca-770">311</span><span class="sxs-lookup"><span data-stu-id="dfdca-770">311</span></span>

[<span data-ttu-id="dfdca-771">筆跡支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-772">312</span><span class="sxs-lookup"><span data-stu-id="dfdca-772">312</span></span>

[<span data-ttu-id="dfdca-773">手寫辨識</span><span class="sxs-lookup"><span data-stu-id="dfdca-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-774">背景智慧型傳送服務 (位) -功能 (335) </span><span class="sxs-lookup"><span data-stu-id="dfdca-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="dfdca-775">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-775">Value</span></span>

<span data-ttu-id="dfdca-776">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-776">Name</span></span>

<span data-ttu-id="dfdca-777">54</span><span class="sxs-lookup"><span data-stu-id="dfdca-777">54</span></span>

<span data-ttu-id="dfdca-778">IIS 伺服器擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-778">IIS Server Extension</span></span>

<span data-ttu-id="dfdca-779">332</span><span class="sxs-lookup"><span data-stu-id="dfdca-779">332</span></span>

[<span data-ttu-id="dfdca-780">Compact Server</span><span class="sxs-lookup"><span data-stu-id="dfdca-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-781">Wow64 支援-功能 (340) </span><span class="sxs-lookup"><span data-stu-id="dfdca-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="dfdca-782">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-782">Value</span></span>

<span data-ttu-id="dfdca-783">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-783">Name</span></span>

<span data-ttu-id="dfdca-784">341</span><span class="sxs-lookup"><span data-stu-id="dfdca-784">341</span></span>

[<span data-ttu-id="dfdca-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="dfdca-786">342</span><span class="sxs-lookup"><span data-stu-id="dfdca-786">342</span></span>

[<span data-ttu-id="dfdca-787">.NET Framework 2.0 和 Windows PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-788">343</span><span class="sxs-lookup"><span data-stu-id="dfdca-788">343</span></span>

[<span data-ttu-id="dfdca-789">.NET Framework 2.0 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-790">344</span><span class="sxs-lookup"><span data-stu-id="dfdca-790">344</span></span>

[<span data-ttu-id="dfdca-791">適用于 PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-792">345</span><span class="sxs-lookup"><span data-stu-id="dfdca-792">345</span></span>

[<span data-ttu-id="dfdca-793">.NET Framework 3.0 和3.5 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-794">346</span><span class="sxs-lookup"><span data-stu-id="dfdca-794">346</span></span>

[<span data-ttu-id="dfdca-795">列印服務的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-796">347</span><span class="sxs-lookup"><span data-stu-id="dfdca-796">347</span></span>

[<span data-ttu-id="dfdca-797">用於容錯移轉叢集的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-798">348</span><span class="sxs-lookup"><span data-stu-id="dfdca-798">348</span></span>

[<span data-ttu-id="dfdca-799">輸入法編輯器的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-800">349</span><span class="sxs-lookup"><span data-stu-id="dfdca-800">349</span></span>

[<span data-ttu-id="dfdca-801">以 UNIX 為基礎之應用程式子系統的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="dfdca-802">使用者介面和基礎結構-角色服務 (447) </span><span class="sxs-lookup"><span data-stu-id="dfdca-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="dfdca-803">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-803">Value</span></span>

<span data-ttu-id="dfdca-804">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-804">Name</span></span>

<span data-ttu-id="dfdca-805">35</span><span class="sxs-lookup"><span data-stu-id="dfdca-805">35</span></span>

[<span data-ttu-id="dfdca-806">桌面體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="dfdca-807">99</span><span class="sxs-lookup"><span data-stu-id="dfdca-807">99</span></span>

[<span data-ttu-id="dfdca-808">伺服器圖形化 Shell</span><span class="sxs-lookup"><span data-stu-id="dfdca-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="dfdca-809">Windows Server Update Services-功能 (404) </span><span class="sxs-lookup"><span data-stu-id="dfdca-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="dfdca-810">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-810">Value</span></span>

<span data-ttu-id="dfdca-811">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-811">Name</span></span>

<span data-ttu-id="dfdca-812">405</span><span class="sxs-lookup"><span data-stu-id="dfdca-812">405</span></span>

[<span data-ttu-id="dfdca-813">API 和 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfdca-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="dfdca-814">406</span><span class="sxs-lookup"><span data-stu-id="dfdca-814">406</span></span>

[<span data-ttu-id="dfdca-815">SQL Server 連線能力</span><span class="sxs-lookup"><span data-stu-id="dfdca-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="dfdca-816">407</span><span class="sxs-lookup"><span data-stu-id="dfdca-816">407</span></span>

[<span data-ttu-id="dfdca-817">WSUS 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="dfdca-818">408</span><span class="sxs-lookup"><span data-stu-id="dfdca-818">408</span></span>

[<span data-ttu-id="dfdca-819">消費者介面管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="dfdca-820">449</span><span class="sxs-lookup"><span data-stu-id="dfdca-820">449</span></span>

[<span data-ttu-id="dfdca-821">WID 連線能力</span><span class="sxs-lookup"><span data-stu-id="dfdca-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="dfdca-822">Windows PowerShell-功能 (417) </span><span class="sxs-lookup"><span data-stu-id="dfdca-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="dfdca-823">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-823">Value</span></span>

<span data-ttu-id="dfdca-824">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-824">Name</span></span>

<span data-ttu-id="dfdca-825">411</span><span class="sxs-lookup"><span data-stu-id="dfdca-825">411</span></span>

[<span data-ttu-id="dfdca-826">Windows PowerShell 2.0 引擎</span><span class="sxs-lookup"><span data-stu-id="dfdca-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="dfdca-827">412</span><span class="sxs-lookup"><span data-stu-id="dfdca-827">412</span></span>

[<span data-ttu-id="dfdca-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="dfdca-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="dfdca-829">448</span><span class="sxs-lookup"><span data-stu-id="dfdca-829">448</span></span>

[<span data-ttu-id="dfdca-830">Windows PowerShell Web 存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="dfdca-831">1000</span><span class="sxs-lookup"><span data-stu-id="dfdca-831">1000</span></span>

[<span data-ttu-id="dfdca-832">Windows PowerShell Desired State Configuration 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="dfdca-833">.NET Framework 4.5-功能 (418) </span><span class="sxs-lookup"><span data-stu-id="dfdca-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="dfdca-834">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-834">Value</span></span>

<span data-ttu-id="dfdca-835">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-835">Name</span></span>

<span data-ttu-id="dfdca-836">419</span><span class="sxs-lookup"><span data-stu-id="dfdca-836">419</span></span>

[<span data-ttu-id="dfdca-837">.NET Framework 4.5 擴充</span><span class="sxs-lookup"><span data-stu-id="dfdca-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="dfdca-838">420</span><span class="sxs-lookup"><span data-stu-id="dfdca-838">420</span></span>

[<span data-ttu-id="dfdca-839">WCF 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-839">WCF Services</span></span>](/windows)

<span data-ttu-id="dfdca-840">421</span><span class="sxs-lookup"><span data-stu-id="dfdca-840">421</span></span>

[<span data-ttu-id="dfdca-841">HTTP 啟動</span><span class="sxs-lookup"><span data-stu-id="dfdca-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="dfdca-842">422</span><span class="sxs-lookup"><span data-stu-id="dfdca-842">422</span></span>

[<span data-ttu-id="dfdca-843">訊息佇列 (MSMQ) 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="dfdca-844">423</span><span class="sxs-lookup"><span data-stu-id="dfdca-844">423</span></span>

[<span data-ttu-id="dfdca-845">具名管道啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="dfdca-846">424</span><span class="sxs-lookup"><span data-stu-id="dfdca-846">424</span></span>

[<span data-ttu-id="dfdca-847">TCP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="dfdca-848">425</span><span class="sxs-lookup"><span data-stu-id="dfdca-848">425</span></span>

[<span data-ttu-id="dfdca-849">TCP 連接埠共用</span><span class="sxs-lookup"><span data-stu-id="dfdca-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="dfdca-850">429</span><span class="sxs-lookup"><span data-stu-id="dfdca-850">429</span></span>

[<span data-ttu-id="dfdca-851">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="dfdca-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="dfdca-852">遠端存取-角色 (468) </span><span class="sxs-lookup"><span data-stu-id="dfdca-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="dfdca-853">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-853">Value</span></span>

<span data-ttu-id="dfdca-854">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-854">Name</span></span>

<span data-ttu-id="dfdca-855">469</span><span class="sxs-lookup"><span data-stu-id="dfdca-855">469</span></span>

[<span data-ttu-id="dfdca-856">DirectAccess 和 VPN (RAS) </span><span class="sxs-lookup"><span data-stu-id="dfdca-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="dfdca-857">470</span><span class="sxs-lookup"><span data-stu-id="dfdca-857">470</span></span>

[<span data-ttu-id="dfdca-858">路由</span><span class="sxs-lookup"><span data-stu-id="dfdca-858">Routing</span></span>](#routing)

<span data-ttu-id="dfdca-859">檔案和存放服務-角色 (481) </span><span class="sxs-lookup"><span data-stu-id="dfdca-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="dfdca-860">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-860">Value</span></span>

<span data-ttu-id="dfdca-861">名稱</span><span class="sxs-lookup"><span data-stu-id="dfdca-861">Name</span></span>

<span data-ttu-id="dfdca-862">482</span><span class="sxs-lookup"><span data-stu-id="dfdca-862">482</span></span>

[<span data-ttu-id="dfdca-863">儲存體服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-863">Storage Services</span></span>](/windows)

<span data-ttu-id="dfdca-864">484</span><span class="sxs-lookup"><span data-stu-id="dfdca-864">484</span></span>

[<span data-ttu-id="dfdca-865">容錯移轉叢集管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="dfdca-866">**名稱**</span><span class="sxs-lookup"><span data-stu-id="dfdca-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfdca-867">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dfdca-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfdca-868">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dfdca-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dfdca-869">伺服器功能的顯示名稱，例如「檔案伺服器」、「列印伺服器」或「桌面體驗」。</span><span class="sxs-lookup"><span data-stu-id="dfdca-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dfdca-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfdca-871">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfdca-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfdca-872">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dfdca-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dfdca-873">父伺服器功能的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfdca-873">ID number of the parent server feature.</span></span> <span data-ttu-id="dfdca-874">如果類別的目前實例所代表的功能沒有父項功能，則這個屬性為0。</span><span class="sxs-lookup"><span data-stu-id="dfdca-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfdca-875">備註</span><span class="sxs-lookup"><span data-stu-id="dfdca-875">Remarks</span></span>

<span data-ttu-id="dfdca-876">閱讀 [Windows Server 2008 伺服器管理員技術總覽](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) ，以瞭解伺服器功能。</span><span class="sxs-lookup"><span data-stu-id="dfdca-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="dfdca-877">未使用管理軟體的企業（例如安裝的管理元件 System Center Operations Manager）可以藉由查詢 **Win32 \_ ServerFeature** 類別來取得該資訊。</span><span class="sxs-lookup"><span data-stu-id="dfdca-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="dfdca-878">您可以使用 WMI 或 WinRM 的遠端功能，從遠端伺服器取得伺服器功能資訊。</span><span class="sxs-lookup"><span data-stu-id="dfdca-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="dfdca-879">如需遠端 WMI DCOM 連接的詳細資訊，請參閱 [連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="dfdca-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="dfdca-880">如需有關 WinRM 的詳細資訊，請參閱 Windows 遠端管理。</span><span class="sxs-lookup"><span data-stu-id="dfdca-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="dfdca-881">Windows Server 2012： **Win32 \_ ServerFeature** 已被取代。</span><span class="sxs-lookup"><span data-stu-id="dfdca-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="dfdca-882">若要以程式設計方式存取 windows server 功能資訊，您可以使用 [伺服器管理員 Cmdlet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="dfdca-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="dfdca-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dfdca-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="dfdca-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>應用程式伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-885">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>串流處理媒體服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-887">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory 同盟服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-889">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-891">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-893">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-895">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-897">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>容錯移轉叢集</span><span class="sxs-lookup"><span data-stu-id="dfdca-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-899">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>網路負載平衡</span><span class="sxs-lookup"><span data-stu-id="dfdca-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-901">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-903">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows 系統 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="dfdca-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-905">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-907">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>遠端協助</span><span class="sxs-lookup"><span data-stu-id="dfdca-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-909">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-911">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-913">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>以 Unix 為基礎的應用程式子系統</span><span class="sxs-lookup"><span data-stu-id="dfdca-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-915">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows 內部資料庫</span><span class="sxs-lookup"><span data-stu-id="dfdca-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-917">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>San 存放管理員</span><span class="sxs-lookup"><span data-stu-id="dfdca-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-919">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>網際網路存放裝置名稱伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-921">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>多重路徑 i/o</span><span class="sxs-lookup"><span data-stu-id="dfdca-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-923">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-925">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>適用于網路檔案系統的服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-927">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>對等名稱解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-929">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>遠端伺服器管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-931">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>高品質的 Windows 音訊影片體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-933">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>群組原則管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-935">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>索引服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-937">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>檔案伺服器 Resource Manager (FSRM) </span><span class="sxs-lookup"><span data-stu-id="dfdca-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-939">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server 移轉工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-941">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="dfdca-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-943">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-945">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>背景智慧型傳送服務 (位) </span><span class="sxs-lookup"><span data-stu-id="dfdca-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-947">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-949">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-951">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP 位址管理 (IPAM) Server</span><span class="sxs-lookup"><span data-stu-id="dfdca-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-953">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfdca-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-955">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4。5</span><span class="sxs-lookup"><span data-stu-id="dfdca-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-957">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-959">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>NFS 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-961">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker 網路解除鎖定</span><span class="sxs-lookup"><span data-stu-id="dfdca-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-963">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>管理 OData IIS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-965">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-967">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-969">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>使用者介面和基礎結構</span><span class="sxs-lookup"><span data-stu-id="dfdca-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-971">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>圖形化管理工具與基礎結構</span><span class="sxs-lookup"><span data-stu-id="dfdca-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-973">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>檔案和存放服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-975">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials 體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-977">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>直接播放</span><span class="sxs-lookup"><span data-stu-id="dfdca-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-979">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>分散式檔案系統</span><span class="sxs-lookup"><span data-stu-id="dfdca-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-981">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>檔案伺服器 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="dfdca-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-983">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>適用于網路檔案系統的服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-985">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>儲存單一版本</span><span class="sxs-lookup"><span data-stu-id="dfdca-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-987">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-989">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>索引服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-991">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI 目標儲存提供者 (VDS 和 VSS 硬體提供者) </span><span class="sxs-lookup"><span data-stu-id="dfdca-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-993">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾</span><span class="sxs-lookup"><span data-stu-id="dfdca-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-995">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory 網網域控制站</span><span class="sxs-lookup"><span data-stu-id="dfdca-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-997">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Unix 身分識別管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-999">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>網路資訊服務的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1001">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>密碼同步化</span><span class="sxs-lookup"><span data-stu-id="dfdca-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1003">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1005">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media 伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1007">不再支援。</span><span class="sxs-lookup"><span data-stu-id="dfdca-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>以網路為基礎的系統管理</span><span class="sxs-lookup"><span data-stu-id="dfdca-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1009">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>記錄代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1011">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>同盟服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1013">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>同盟服務原則</span><span class="sxs-lookup"><span data-stu-id="dfdca-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1015">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web 代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1017">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows 權杖型代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1019">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>遠端桌面授權</span><span class="sxs-lookup"><span data-stu-id="dfdca-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1021">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1023">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1024"><span id="VPN"></span><span id="vpn"></span>Vpn</span><span class="sxs-lookup"><span data-stu-id="dfdca-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1025">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1027">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>路由</span><span class="sxs-lookup"><span data-stu-id="dfdca-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1029">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>健康情況登錄授權單位</span><span class="sxs-lookup"><span data-stu-id="dfdca-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1031">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>主機認證授權通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1033">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5。1</span><span class="sxs-lookup"><span data-stu-id="dfdca-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1035">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS 檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1037">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1039">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="dfdca-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1041">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5。1</span><span class="sxs-lookup"><span data-stu-id="dfdca-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1043">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span> (IIS) 支援的 Web 服務器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1045">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM + 網路存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1047">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP 埠共用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1049">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows 處理常式啟用服務支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1051">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1053">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>訊息佇列啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1055">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1057">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>具名管道啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1059">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>分散式交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1061">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>傳入遠端交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1063">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>連出遠端交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1065">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-自動交易</span><span class="sxs-lookup"><span data-stu-id="dfdca-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1067">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>適用于 .NET 4.0 的應用程式伺服器擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1069">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>角色管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1071">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1073">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1075">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>網路原則與存取服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1077">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="dfdca-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1079">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>遠端桌面服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1081">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>功能管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1083">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>容錯移轉叢集工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1085">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS 伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1087">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1089">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web 服務器 (IIS) 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1091">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1093">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1095">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1097">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>遠端桌面連線代理人工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1099">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP 位址管理 (IPAM) 用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1101">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Windows PowerShell 的 hyper-v 模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dfdca-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1104">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>共用與存放管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1106">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>遠端存取管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1108">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Windows PowerShell 的遠端存取模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1110">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>遠端存取 GUI 和 Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1112">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1114">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>遠端桌面授權診斷程式工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1116">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1118">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>大量啟用工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1120">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="dfdca-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1122">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>命令列工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1124">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>筆跡支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1126">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>手寫辨識</span><span class="sxs-lookup"><span data-stu-id="dfdca-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1128">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span><span class="sxs-lookup"><span data-stu-id="dfdca-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1130">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1132">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>適用于 .NET Framework 2.0 和 PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1134">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>.NET Framework 2.0 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1136">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>適用于 PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1138">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>.NET Framework 3.0 和3.5 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1140">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>列印服務的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1142">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>用於容錯移轉叢集的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1144">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>輸入法編輯器的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1146">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>以 UNIX 為基礎之應用程式子系統的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1148">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>桌面體驗</span><span class="sxs-lookup"><span data-stu-id="dfdca-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1150">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>伺服器圖形化 Shell</span><span class="sxs-lookup"><span data-stu-id="dfdca-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1152">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API 和 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfdca-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1154">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server 連線能力</span><span class="sxs-lookup"><span data-stu-id="dfdca-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1156">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1158">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>消費者介面管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1160">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID 連線能力</span><span class="sxs-lookup"><span data-stu-id="dfdca-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1162">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 引擎</span><span class="sxs-lookup"><span data-stu-id="dfdca-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1164">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3。0</span><span class="sxs-lookup"><span data-stu-id="dfdca-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1166">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web 存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1168">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1170">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 擴充</span><span class="sxs-lookup"><span data-stu-id="dfdca-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1172">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1174">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1176">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>訊息佇列 (MSMQ) 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dfdca-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>具名管道啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1179">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP 啟用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1181">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP 埠共用</span><span class="sxs-lookup"><span data-stu-id="dfdca-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1183">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4。5</span><span class="sxs-lookup"><span data-stu-id="dfdca-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1185">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET 擴充性4。5</span><span class="sxs-lookup"><span data-stu-id="dfdca-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1187">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess 和 VPN (RAS) </span><span class="sxs-lookup"><span data-stu-id="dfdca-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1189">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>路由</span><span class="sxs-lookup"><span data-stu-id="dfdca-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1191">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>儲存體服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1193">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>容錯移轉叢集管理工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1195">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1197">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>應用程式初始化</span><span class="sxs-lookup"><span data-stu-id="dfdca-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1199">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>集中式 SSL 憑證支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1201">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>宣告感知代理程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1203">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>遠端桌面工作階段主機工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1205">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket 通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfdca-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1207">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM + 網路存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1209">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>檔案和 iSCSI 服務名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1211">已變更為檔案服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="dfdca-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfdca-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="dfdca-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>使用者介面和基礎結構</span><span class="sxs-lookup"><span data-stu-id="dfdca-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1214">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span><span class="sxs-lookup"><span data-stu-id="dfdca-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1216">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>檔案伺服器 VSS 代理程式服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1218">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI 目標伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1220">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>重復資料刪除</span><span class="sxs-lookup"><span data-stu-id="dfdca-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1222">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾</span><span class="sxs-lookup"><span data-stu-id="dfdca-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1224">移除</span><span class="sxs-lookup"><span data-stu-id="dfdca-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>核心服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1226">僅針對此版本新增。</span><span class="sxs-lookup"><span data-stu-id="dfdca-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>遠端桌面虛擬圖形</span><span class="sxs-lookup"><span data-stu-id="dfdca-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1228">僅針對此版本新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>遠端存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1230">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="dfdca-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfdca-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="dfdca-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1233">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows 系統 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="dfdca-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1235">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>卸除式存放裝置管理員</span><span class="sxs-lookup"><span data-stu-id="dfdca-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1237">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dfdca-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1239">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>筆跡和手寫服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1241">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1243">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1245">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>背景智慧型傳送服務 (位) </span><span class="sxs-lookup"><span data-stu-id="dfdca-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1247">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS 檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1249">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows 生物特徵辨識架構</span><span class="sxs-lookup"><span data-stu-id="dfdca-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1251">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1253">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell (ISE) 的整合式腳本環境</span><span class="sxs-lookup"><span data-stu-id="dfdca-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1255">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>檔案複寫服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1257">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>網路檔案的 BranchCache</span><span class="sxs-lookup"><span data-stu-id="dfdca-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1259">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾</span><span class="sxs-lookup"><span data-stu-id="dfdca-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1261">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>分散式掃描伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1263">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP 發行服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1265">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP 管理主控台</span><span class="sxs-lookup"><span data-stu-id="dfdca-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1267">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1269">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP 擴充性</span><span class="sxs-lookup"><span data-stu-id="dfdca-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1271">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS 裝載的 Web 核心</span><span class="sxs-lookup"><span data-stu-id="dfdca-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="dfdca-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 用戶端支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1274">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>憑證註冊 Web 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1276">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>憑證註冊原則 Web 服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1278">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI 服務 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1280">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI 服務資料庫</span><span class="sxs-lookup"><span data-stu-id="dfdca-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1282">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>適用于 .NET 4.0 的應用程式伺服器擴充功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1284">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI 服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1286">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker 磁碟機加密管理公用程式</span><span class="sxs-lookup"><span data-stu-id="dfdca-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1288">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1290">不再支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1292">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory 管理中心</span><span class="sxs-lookup"><span data-stu-id="dfdca-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1294">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>適用于 Windows PowerShell 的 Active Directory 模組</span><span class="sxs-lookup"><span data-stu-id="dfdca-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1296">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>遠端桌面連線代理人工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1298">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1300">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>.NET Framework 2.0 和 Windows PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1302">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>.NET Framework 2.0 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1304">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>適用于 PowerShell 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1306">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>.NET Framework 3.0 和3.5 的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1308">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>列印服務的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1310">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>用於容錯移轉叢集的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1312">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>輸入法編輯器的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1314">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>以 UNIX 為基礎之應用程式子系統的 WoW64</span><span class="sxs-lookup"><span data-stu-id="dfdca-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1316">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker 修復密碼檢視器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1318">已新增</span><span class="sxs-lookup"><span data-stu-id="dfdca-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>列印和檔服務名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1320">此版本的命名列印服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>遠端桌面服務名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1322">此版本中命名的終端機服務</span><span class="sxs-lookup"><span data-stu-id="dfdca-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 功能名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1324">此版本中的命名 .NET Framework 3.0 功能</span><span class="sxs-lookup"><span data-stu-id="dfdca-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>遠端桌面工作階段主機名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1326">此版本中命名的終端機伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>遠端桌面授權名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1328">此版本中的命名為 TS 授權</span><span class="sxs-lookup"><span data-stu-id="dfdca-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>遠端桌面閘道名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1330">此版本中的命名為 TS 閘道</span><span class="sxs-lookup"><span data-stu-id="dfdca-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>遠端桌面連線代理人名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1332">此版本中的命名為 TS Session Broker</span><span class="sxs-lookup"><span data-stu-id="dfdca-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>遠端桌面 Web 存取名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1334">此版本中名為 TS Web 存取</span><span class="sxs-lookup"><span data-stu-id="dfdca-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1336">此版本中名為 Net FX 3.0 功能的 (220) </span><span class="sxs-lookup"><span data-stu-id="dfdca-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="dfdca-1337">在此版本中，名為 Application Server Core 的 (230) </span><span class="sxs-lookup"><span data-stu-id="dfdca-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS 工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1339">此版本中的命名 Active Directory Domain Services 工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins 和 Command-Line 工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1341">此版本中的命名 Active Directory 輕量型目錄服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>列印和檔服務工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1343">此版本中的命名列印服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>遠端桌面服務工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1345">此版本中命名的終端機服務工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>遠端桌面工作階段主機工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1347">此版本中命名的終端機伺服器工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>遠端桌面閘道工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1349">此版本中命名的 TS 閘道工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>遠端桌面授權工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1351">此版本中命名的 TS 授權工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="dfdca-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins 和 Command-Line 工具名稱變更</span><span class="sxs-lookup"><span data-stu-id="dfdca-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="dfdca-1353">Active Directory 網域控制站工具</span><span class="sxs-lookup"><span data-stu-id="dfdca-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="dfdca-1354">範例</span><span class="sxs-lookup"><span data-stu-id="dfdca-1354">Examples</span></span>

<span data-ttu-id="dfdca-1355">下列腳本會顯示名為 "FABRIKAM" 的電腦上所有伺服器功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfdca-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="dfdca-1356">請注意，目的電腦必須執行 Windows Server 2008 或更新版本的伺服器作業系統。</span><span class="sxs-lookup"><span data-stu-id="dfdca-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="dfdca-1357">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfdca-1357">Requirements</span></span>



| <span data-ttu-id="dfdca-1358">需求</span><span class="sxs-lookup"><span data-stu-id="dfdca-1358">Requirement</span></span> | <span data-ttu-id="dfdca-1359">值</span><span class="sxs-lookup"><span data-stu-id="dfdca-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdca-1360">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfdca-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="dfdca-1361">都不支援</span><span class="sxs-lookup"><span data-stu-id="dfdca-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dfdca-1362">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfdca-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="dfdca-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfdca-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="dfdca-1364">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfdca-1364">Namespace</span></span><br/>                | <span data-ttu-id="dfdca-1365">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfdca-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="dfdca-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="dfdca-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfdca-1367"><dt>ServerCompProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfdca-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfdca-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="dfdca-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfdca-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfdca-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

