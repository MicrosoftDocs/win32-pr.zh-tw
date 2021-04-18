---
title: 搭配 Exchange 使用 ADSI
description: 若為 Exchange 2000，將 ADSI 與 Exchange 搭配使用的資訊包含在 Exchange 2000 SDK 中。 如需詳細資訊，請參閱 ADSI 的管理工作。
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI for Exchange ADSI
- ADSI for Exchange ADSI，信箱
- ADSI for Exchange ADSI、信箱、建立
- ADSI for Exchange ADSI、信箱、刪除
- ADSI for Exchange ADSI、信箱、設定安全描述項
- ADSI for Exchange ADSI、信箱、尋找 home server for
- ADSI for Exchange ADSI，取得和修改訊息
- ADSI for Exchange ADSI，安全描述項
- ADSI for Exchange ADSI、安全描述項、操作
- ADSI for Exchange ADSI，安全描述項，設定
- ADSI for Exchange ADSI，收件者容器
- ADSI for Exchange ADSI，查看 Exchange 物件屬性
- ADSI for Exchange ADSI、接收者容器、自訂
- ADSI for Exchange ADSI，Exchange Server
- ADSI for Exchange ADSI、Exchange Server、流覽和修改架構
- ADSI for Exchange ADSI、Exchange Server、清單伺服器版本
- ADSI for Exchange ADSI、Exchange Server、組織和網站名稱
- ADSI for Exchange ADSI、Exchange Server、尋找信箱首頁伺服器
- ADSI for Exchange ADSI，電子郵件地址，正在抓取
- ADSI for Exchange ADSI、通訊群組清單、建立
- ADSI for Exchange ADSI、隱藏或刪除的專案
- ADSI for Exchange ADSI，正在取得目錄服務變更
- ADSI for Exchange ADSI，訊息大小
- ADSI for Exchange ADSI，疑難排解問題
- 信箱 ADSI
- 信箱 ADSI，建立
- 信箱 ADSI，刪除
- 信箱 ADSI，設定安全描述項
- 信箱： ADSI，尋找 home server
- 訊息 ADSI、取得和修改
- Exchange ADSI
- Exchange ADSI，信箱
- Exchange ADSI，信箱，建立
- Exchange ADSI，信箱，刪除
- Exchange ADSI，信箱，設定安全描述項于
- Exchange ADSI、信箱、尋找 home server
- Exchange ADSI，取得和修改訊息
- Exchange ADSI，安全描述項
- Exchange ADSI，安全描述項，操作
- Exchange ADSI，安全描述項，設定
- Exchange ADSI，收件者容器
- Exchange ADSI，查看 Exchange 物件屬性
- Exchange ADSI，收件者容器，自訂
- Exchange ADSI、Exchange Server
- Exchange ADSI、Exchange Server、流覽和修改架構
- Exchange ADSI、Exchange Server、清單伺服器版本
- Exchange ADSI、Exchange Server、組織和網站名稱
- Exchange ADSI、Exchange Server、尋找信箱首頁伺服器
- Exchange ADSI，電子郵件地址，正在抓取
- Exchange ADSI，通訊群組清單，建立
- Exchange ADSI、隱藏或刪除的專案
- Exchange ADSI，正在進行目錄服務變更
- Exchange ADSI，訊息大小
- Exchange ADSI，疑難排解問題
- 適用于 Exchange 物件的安全描述項 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968720"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="a745b-159">搭配 Exchange 使用 ADSI</span><span class="sxs-lookup"><span data-stu-id="a745b-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="a745b-160">若為 Exchange 2000，將 ADSI 與 Exchange 搭配使用的資訊包含在 Exchange 2000 SDK 中。</span><span class="sxs-lookup"><span data-stu-id="a745b-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="a745b-161">如需詳細資訊，請參閱 [ADSI 的管理](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65))工作。</span><span class="sxs-lookup"><span data-stu-id="a745b-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="a745b-162">您可以在本節中找到下列工作：</span><span class="sxs-lookup"><span data-stu-id="a745b-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="a745b-163">建立使用者 URL</span><span class="sxs-lookup"><span data-stu-id="a745b-163">Creating a user URL</span></span>
-   <span data-ttu-id="a745b-164">建立 Active Directory 路徑</span><span class="sxs-lookup"><span data-stu-id="a745b-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="a745b-165">使用 ADSI 列舉 Exchange 2000 伺服器</span><span class="sxs-lookup"><span data-stu-id="a745b-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="a745b-166">使用 ADSI 操控擴充屬性</span><span class="sxs-lookup"><span data-stu-id="a745b-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="a745b-167">使用 ADSI 新增/移除管理員物件</span><span class="sxs-lookup"><span data-stu-id="a745b-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="a745b-168">使用 ADSI/ADO 列舉 Exchange 物件屬性</span><span class="sxs-lookup"><span data-stu-id="a745b-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="a745b-169">使用 ADSI 抓取舊版 Exchange 辨別名稱</span><span class="sxs-lookup"><span data-stu-id="a745b-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="a745b-170">使用 ADSI 尋找 Exchange 組織名稱</span><span class="sxs-lookup"><span data-stu-id="a745b-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="a745b-171">使用 ADSI 尋找 Exchange 通訊清單</span><span class="sxs-lookup"><span data-stu-id="a745b-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="a745b-172">使用 CDOEXM 和 ADSI 建立通訊群組清單</span><span class="sxs-lookup"><span data-stu-id="a745b-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="a745b-173">使用 ADSI 在 SMTP 虛擬伺服器上設定訊息限制</span><span class="sxs-lookup"><span data-stu-id="a745b-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="a745b-174">若為 Exchange 5.5，adsi 參考和使用資訊可在 [Adsi Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) 指南中找到。</span><span class="sxs-lookup"><span data-stu-id="a745b-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="a745b-175">您可以在本節中找到下列工作：</span><span class="sxs-lookup"><span data-stu-id="a745b-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="a745b-176">查看和修改 Exchange Server 架構</span><span class="sxs-lookup"><span data-stu-id="a745b-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="a745b-177">查看 Exchange 物件的原始屬性</span><span class="sxs-lookup"><span data-stu-id="a745b-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="a745b-178">建立 Exchange 信箱</span><span class="sxs-lookup"><span data-stu-id="a745b-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="a745b-179">設定 Exchange 信箱上的安全描述項</span><span class="sxs-lookup"><span data-stu-id="a745b-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="a745b-180">操作安全描述項和 Sid</span><span class="sxs-lookup"><span data-stu-id="a745b-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="a745b-181">刪除信箱物件</span><span class="sxs-lookup"><span data-stu-id="a745b-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="a745b-182">建立自訂的收件者</span><span class="sxs-lookup"><span data-stu-id="a745b-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="a745b-183">建立收件者容器</span><span class="sxs-lookup"><span data-stu-id="a745b-183">Creating a recipients container</span></span>
-   <span data-ttu-id="a745b-184">從伺服器取得組織和網站名稱</span><span class="sxs-lookup"><span data-stu-id="a745b-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="a745b-185">列出組織中所有伺服器的 Exchange server 版本</span><span class="sxs-lookup"><span data-stu-id="a745b-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="a745b-186">尋找信箱的主伺服器</span><span class="sxs-lookup"><span data-stu-id="a745b-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="a745b-187">正在抓取電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="a745b-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="a745b-188">存取隱藏或刪除的專案</span><span class="sxs-lookup"><span data-stu-id="a745b-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="a745b-189">正在抓取對目錄服務所做的變更</span><span class="sxs-lookup"><span data-stu-id="a745b-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="a745b-190">從查詢結果建立通訊群組清單</span><span class="sxs-lookup"><span data-stu-id="a745b-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="a745b-191">取得或修改訊息大小</span><span class="sxs-lookup"><span data-stu-id="a745b-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="a745b-192">使用 LDAP 錯誤碼針對問題進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="a745b-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 