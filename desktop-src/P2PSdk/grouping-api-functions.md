---
description: 群組 API 會使用下列功能：
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: 群組 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976904"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="d47ad-103">群組 API 函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-103">Grouping API Functions</span></span>

<span data-ttu-id="d47ad-104">群組 API 會使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="d47ad-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="d47ad-105">群組初始化和清除函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="d47ad-106">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-106">Function</span></span>                                       | <span data-ttu-id="d47ad-107">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-108">**PeerGroupShutdown**</span><span class="sxs-lookup"><span data-stu-id="d47ad-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="d47ad-109">關閉使用 [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) 所建立的對等群組，並處置任何已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="d47ad-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="d47ad-110">**PeerGroupStartup**</span><span class="sxs-lookup"><span data-stu-id="d47ad-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="d47ad-111">使用要求的對等基礎結構版本，初始化對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="d47ad-112">群組建立和存取功能</span><span class="sxs-lookup"><span data-stu-id="d47ad-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="d47ad-113">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-113">Function</span></span>                                                                       | <span data-ttu-id="d47ad-114">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-115">**PeerGroupClose**</span><span class="sxs-lookup"><span data-stu-id="d47ad-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="d47ad-116">使先前呼叫 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)、 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)或 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) 函數所取得的對等群組控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="d47ad-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="d47ad-117">**PeerGroupConnect**</span><span class="sxs-lookup"><span data-stu-id="d47ad-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="d47ad-118">初始化對等群組的 PNRP 搜尋，並嘗試連接到該群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="d47ad-119">成功呼叫這個函式之後，對等可以與對等群組的其他成員進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d47ad-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="d47ad-120">**PeerGroupConnectByAddress**</span><span class="sxs-lookup"><span data-stu-id="d47ad-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="d47ad-121">嘗試連接到具有已知 IPv6 位址的其他對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="d47ad-122">**PeerGroupCreate**</span><span class="sxs-lookup"><span data-stu-id="d47ad-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="d47ad-123">建立新的對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="d47ad-124">**PeerGroupCreateInvitation**</span><span class="sxs-lookup"><span data-stu-id="d47ad-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="d47ad-125">傳回可供指定的對等聯結群組的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="d47ad-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="d47ad-126">**PeerGroupCreatePasswordInvitation**</span><span class="sxs-lookup"><span data-stu-id="d47ad-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="d47ad-127">傳回 XML 字串，這個字串可供指定的對等聯結使用相符密碼的群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="d47ad-128">**PeerGroupDelete**</span><span class="sxs-lookup"><span data-stu-id="d47ad-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="d47ad-129">刪除與對等群組相關聯的本機資料和憑證。</span><span class="sxs-lookup"><span data-stu-id="d47ad-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="d47ad-130">**PeerGroupGetStatus**</span><span class="sxs-lookup"><span data-stu-id="d47ad-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="d47ad-131">抓取群組的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d47ad-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="d47ad-132">**PeerGroupIssueCredentials**</span><span class="sxs-lookup"><span data-stu-id="d47ad-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="d47ad-133">將認證（包括 GMC）發行至特定身分識別，並選擇性地傳回受邀的對等互連可用於加入對等群組的邀請 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="d47ad-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="d47ad-134">**PeerGroupJoin**</span><span class="sxs-lookup"><span data-stu-id="d47ad-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="d47ad-135">允許對等的邀請加入現有的對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="d47ad-136">**PeerGroupOpen**</span><span class="sxs-lookup"><span data-stu-id="d47ad-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="d47ad-137">開啟對等互連已建立或聯結的對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="d47ad-138">**PeerGroupParseInvitation**</span><span class="sxs-lookup"><span data-stu-id="d47ad-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="d47ad-139">傳回 [**對等 \_ 邀請 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) 結構，其中包含特定邀請的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d47ad-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="d47ad-140">**PeerGroupPasswordJoin**</span><span class="sxs-lookup"><span data-stu-id="d47ad-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="d47ad-141">允許對等具有邀請和正確的密碼，以聯結受密碼保護的對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="d47ad-142">群組和成員資訊函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="d47ad-143">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-143">Function</span></span>                                                 | <span data-ttu-id="d47ad-144">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-145">**PeerGroupEnumMembers**</span><span class="sxs-lookup"><span data-stu-id="d47ad-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="d47ad-146">建立可用對等群組成員的列舉，以及相關聯的成員資格資訊。</span><span class="sxs-lookup"><span data-stu-id="d47ad-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="d47ad-147">**PeerGroupGetProperties**</span><span class="sxs-lookup"><span data-stu-id="d47ad-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="d47ad-148">抓取指定群組之屬性的資訊。</span><span class="sxs-lookup"><span data-stu-id="d47ad-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="d47ad-149">**PeerGroupSetProperties**</span><span class="sxs-lookup"><span data-stu-id="d47ad-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="d47ad-150">設定目前的對等群組屬性。</span><span class="sxs-lookup"><span data-stu-id="d47ad-150">Sets the current peer group properties.</span></span> <span data-ttu-id="d47ad-151">在此 API 的1.0 版中，只有對等群組的建立者可以執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="d47ad-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="d47ad-152">記錄和記錄管理功能</span><span class="sxs-lookup"><span data-stu-id="d47ad-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="d47ad-153">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-153">Function</span></span>                                                 | <span data-ttu-id="d47ad-154">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-155">**PeerGroupAddRecord**</span><span class="sxs-lookup"><span data-stu-id="d47ad-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="d47ad-156">將新記錄加入至對等群組，此群組會傳播到所有參與的對等群組。</span><span class="sxs-lookup"><span data-stu-id="d47ad-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="d47ad-157">**PeerGroupDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="d47ad-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="d47ad-158">從對等群組刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="d47ad-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="d47ad-159">只有記錄的建立者可以將其刪除。</span><span class="sxs-lookup"><span data-stu-id="d47ad-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="d47ad-160">**PeerGroupEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="d47ad-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="d47ad-161">建立對等群組記錄的列舉。</span><span class="sxs-lookup"><span data-stu-id="d47ad-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="d47ad-162">**PeerGroupGetRecord**</span><span class="sxs-lookup"><span data-stu-id="d47ad-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="d47ad-163">抓取特定的群組記錄。</span><span class="sxs-lookup"><span data-stu-id="d47ad-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="d47ad-164">**PeerGroupSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="d47ad-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="d47ad-165">搜尋本機對等群組資料庫中是否有符合所提供準則的記錄。</span><span class="sxs-lookup"><span data-stu-id="d47ad-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="d47ad-166">**PeerGroupUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="d47ad-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="d47ad-167">更新特定對等群組內的記錄。</span><span class="sxs-lookup"><span data-stu-id="d47ad-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="d47ad-168">群組資料庫匯入/匯出函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="d47ad-169">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-169">Function</span></span>                                                   | <span data-ttu-id="d47ad-170">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-171">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="d47ad-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="d47ad-172">將對等群組資料庫匯出至特定檔案，該檔案可以傳輸到另一部電腦，並使用 [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) 函式匯入。</span><span class="sxs-lookup"><span data-stu-id="d47ad-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="d47ad-173">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="d47ad-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="d47ad-174">從本機檔案匯入對等群組資料庫。</span><span class="sxs-lookup"><span data-stu-id="d47ad-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="d47ad-175">直接連接函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-175">Direct Connection Functions</span></span>



| <span data-ttu-id="d47ad-176">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-176">Function</span></span>                                                                 | <span data-ttu-id="d47ad-177">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-178">**PeerGroupCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="d47ad-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="d47ad-179">關閉兩個對等之間的特定直接連接。</span><span class="sxs-lookup"><span data-stu-id="d47ad-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="d47ad-180">**PeerGroupEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="d47ad-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="d47ad-181">建立目前對等的作用中連接的列舉。</span><span class="sxs-lookup"><span data-stu-id="d47ad-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="d47ad-182">**PeerGroupOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="d47ad-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="d47ad-183">在對等群組中建立與另一個對等的直接連接。</span><span class="sxs-lookup"><span data-stu-id="d47ad-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="d47ad-184">**PeerGroupSendData**</span><span class="sxs-lookup"><span data-stu-id="d47ad-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="d47ad-185">透過鄰近或直接連線將資料傳送至成員。</span><span class="sxs-lookup"><span data-stu-id="d47ad-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="d47ad-186">群組事件基礎結構</span><span class="sxs-lookup"><span data-stu-id="d47ad-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="d47ad-187">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-187">Function</span></span>                                                     | <span data-ttu-id="d47ad-188">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-189">**PeerGroupGetEventData**</span><span class="sxs-lookup"><span data-stu-id="d47ad-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="d47ad-190">允許應用程式取出群組事件所傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="d47ad-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="d47ad-191">**PeerGroupRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="d47ad-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="d47ad-192">針對特定的對等群組事件註冊對等。</span><span class="sxs-lookup"><span data-stu-id="d47ad-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="d47ad-193">**PeerGroupUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="d47ad-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="d47ad-194">從與提供的事件控制碼相關聯的對等事件的通知中取消註冊對等。</span><span class="sxs-lookup"><span data-stu-id="d47ad-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="d47ad-195">群組時間轉換函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="d47ad-196">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-196">Function</span></span>                                                                     | <span data-ttu-id="d47ad-197">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-198">**PeerGroupPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="d47ad-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="d47ad-199">將對等群組維護的參考時間值轉換成適合在對等電腦上顯示的當地語系化時間值。</span><span class="sxs-lookup"><span data-stu-id="d47ad-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="d47ad-200">**PeerGroupUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="d47ad-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="d47ad-201">將本機時間值從對等電腦轉換為一般對等群組時間值。</span><span class="sxs-lookup"><span data-stu-id="d47ad-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="d47ad-202">群組設定函數</span><span class="sxs-lookup"><span data-stu-id="d47ad-202">Group Configuration Functions</span></span>



| <span data-ttu-id="d47ad-203">函式</span><span class="sxs-lookup"><span data-stu-id="d47ad-203">Function</span></span>                                               | <span data-ttu-id="d47ad-204">描述</span><span class="sxs-lookup"><span data-stu-id="d47ad-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d47ad-205">**PeerGroupExportConfig**</span><span class="sxs-lookup"><span data-stu-id="d47ad-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="d47ad-206">將對等的群組設定匯出為 XML 字串，其中包含身分識別、組名和身分識別的 GMC。</span><span class="sxs-lookup"><span data-stu-id="d47ad-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="d47ad-207">**PeerGroupImportConfig**</span><span class="sxs-lookup"><span data-stu-id="d47ad-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="d47ad-208">根據提供的 XML 設定字串中的特定設定，匯入身分識別的對等群組設定。</span><span class="sxs-lookup"><span data-stu-id="d47ad-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



