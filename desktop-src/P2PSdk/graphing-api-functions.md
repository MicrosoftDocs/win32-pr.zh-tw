---
description: 對等圖形 API 使用下列功能：
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: 圖形 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343f3f5ff1e53180cced98cbebbd66af1d28e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849315"
---
# <a name="graphing-api-functions"></a><span data-ttu-id="f7bfb-103">圖形 API 函數</span><span class="sxs-lookup"><span data-stu-id="f7bfb-103">Graphing API Functions</span></span>

<span data-ttu-id="f7bfb-104">對等圖形 API 使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="f7bfb-104">The Peer Graphing API uses the following functions:</span></span>

## <a name="initialization-and-cleanup-functions"></a><span data-ttu-id="f7bfb-105">初始化和清除函數</span><span class="sxs-lookup"><span data-stu-id="f7bfb-105">Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="f7bfb-106">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-106">Function</span></span>                                       | <span data-ttu-id="f7bfb-107">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-107">Description</span></span>                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-108">**PeerGraphShutdown**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-108">**PeerGraphShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | <span data-ttu-id="f7bfb-109">清除呼叫 [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)所配置的任何資源。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-109">Cleans up any resources allocated by the call to [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup).</span></span>                     |
| [<span data-ttu-id="f7bfb-110">**PeerGraphStartup**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-110">**PeerGraphStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | <span data-ttu-id="f7bfb-111">向對等圖形基礎結構指出呼叫應用程式所需的對等通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-111">Indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.</span></span> |



 

## <a name="graph-creation-and-access-functions"></a><span data-ttu-id="f7bfb-112">圖表建立和存取函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-112">Graph Creation and Access Functions</span></span>



| <span data-ttu-id="f7bfb-113">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-113">Function</span></span>                                   | <span data-ttu-id="f7bfb-114">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-114">Description</span></span>                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-115">**PeerGraphClose**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-115">**PeerGraphClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | <span data-ttu-id="f7bfb-116">使對 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) 或 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)的呼叫所傳回的對等圖形控制碼失效，並關閉指定之對等圖表的所有網路連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-116">Invalidates the peer graph handle returned by a call to either [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) or [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen), and closes all network connections for the specified peer graph.</span></span> |
| [<span data-ttu-id="f7bfb-117">**PeerGraphCreate**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-117">**PeerGraphCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | <span data-ttu-id="f7bfb-118">建立新的對等圖形。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-118">Creates a new peer graph.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="f7bfb-119">**PeerGraphDelete**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-119">**PeerGraphDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | <span data-ttu-id="f7bfb-120">刪除與指定之對等圖形相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-120">Deletes the data associated with a specified peer graph.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="f7bfb-121">**PeerGraphListen**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-121">**PeerGraphListen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | <span data-ttu-id="f7bfb-122">表示對等圖形應開始接聽傳入連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-122">Indicates that a peer graph should start listening for incoming connections.</span></span>                                                                                                                                          |
| [<span data-ttu-id="f7bfb-123">**PeerGraphOpen**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-123">**PeerGraphOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | <span data-ttu-id="f7bfb-124">開啟先前由本機節點或遠端節點所建立的對等圖形。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-124">Opens a peer graph that is created previously by either the local node or a remote node.</span></span>                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a><span data-ttu-id="f7bfb-125">圖形和節點資訊函數</span><span class="sxs-lookup"><span data-stu-id="f7bfb-125">Graph and Node Information Functions</span></span>



| <span data-ttu-id="f7bfb-126">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-126">Function</span></span>                                                         | <span data-ttu-id="f7bfb-127">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-127">Description</span></span>                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-128">**PeerGraphEnumNodes**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-128">**PeerGraphEnumNodes**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | <span data-ttu-id="f7bfb-129">建立並傳回列舉控制碼，用來列舉對等圖形中的節點。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-129">Creates and returns an enumeration handle used to enumerate the nodes in a peer graph.</span></span>                                                                             |
| [<span data-ttu-id="f7bfb-130">**PeerGraphGetNodeInfo**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-130">**PeerGraphGetNodeInfo**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | <span data-ttu-id="f7bfb-131">抓取特定節點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-131">Retrieves information about a specific node.</span></span>                                                                                                                       |
| [<span data-ttu-id="f7bfb-132">**PeerGraphGetProperties**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-132">**PeerGraphGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | <span data-ttu-id="f7bfb-133">抓取目前的對等圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-133">Retrieves the current peer graph properties.</span></span>                                                                                                                       |
| [<span data-ttu-id="f7bfb-134">**PeerGraphGetStatus**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-134">**PeerGraphGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | <span data-ttu-id="f7bfb-135">傳回對等圖形的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-135">Returns the current status of the peer graph.</span></span>                                                                                                                      |
| [<span data-ttu-id="f7bfb-136">**PeerGraphSetNodeAttributes**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-136">**PeerGraphSetNodeAttributes**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | <span data-ttu-id="f7bfb-137">設定本機節點的 [**對等 \_ 節點 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) 結構的屬性。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-137">Sets the attributes of the [**PEER\_NODE\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) structure for the local node.</span></span>                                                                |
| [<span data-ttu-id="f7bfb-138">**PeerGraphSetPresence**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-138">**PeerGraphSetPresence**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | <span data-ttu-id="f7bfb-139">明確開啟或關閉特定節點的狀態記錄發行集。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-139">Explicitly turns on or off the publication of presence records for a specific node.</span></span> <span data-ttu-id="f7bfb-140">此函數可以覆寫對等圖形屬性中的存在性設定。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-140">This function can override the presence settings in the peer graph properties.</span></span> |
| [<span data-ttu-id="f7bfb-141">**PeerGraphSetProperties**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-141">**PeerGraphSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | <span data-ttu-id="f7bfb-142">設定對等圖形屬性。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-142">Sets the peer graph properties.</span></span>                                                                                                                                    |



 

## <a name="record-management-functions"></a><span data-ttu-id="f7bfb-143">記錄管理功能</span><span class="sxs-lookup"><span data-stu-id="f7bfb-143">Record Management Functions</span></span>



| <span data-ttu-id="f7bfb-144">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-144">Function</span></span>                                                                     | <span data-ttu-id="f7bfb-145">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-145">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-146">**PeerGraphAddRecord**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-146">**PeerGraphAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | <span data-ttu-id="f7bfb-147">將新記錄加入至對等圖形。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-147">Adds a new record to a peer graph.</span></span> <span data-ttu-id="f7bfb-148">使用此函式加入的記錄會傳送到對等圖形中的每個節點。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-148">A record added with this function is sent to each node in a peer graph.</span></span>                          |
| [<span data-ttu-id="f7bfb-149">**PeerGraphDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-149">**PeerGraphDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | <span data-ttu-id="f7bfb-150">將記錄標示為在對等圖形內刪除。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-150">Marks a record as deleted within a peer graph.</span></span>                                                                                      |
| [<span data-ttu-id="f7bfb-151">**PeerGraphEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-151">**PeerGraphEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | <span data-ttu-id="f7bfb-152">建立並傳回列舉控制碼，這個控制碼可用來列舉特定記錄類型的記錄、使用者或兩者的記錄。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-152">Creates and returns an enumeration handle used to enumerate records of a specific type of record, user, or both.</span></span>                    |
| [<span data-ttu-id="f7bfb-153">**PeerGraphGetRecord**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-153">**PeerGraphGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | <span data-ttu-id="f7bfb-154">根據指定的記錄識別碼抓取特定記錄。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-154">Retrieves a specific record based on the specified record ID.</span></span>                                                                       |
| [<span data-ttu-id="f7bfb-155">**PeerGraphSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-155">**PeerGraphSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | <span data-ttu-id="f7bfb-156">在對等圖形中搜尋特定記錄。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-156">Searches the peer graph for specific records.</span></span>                                                                                       |
| [<span data-ttu-id="f7bfb-157">**PeerGraphUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-157">**PeerGraphUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | <span data-ttu-id="f7bfb-158">更新對等圖形中的記錄，然後將記錄氾濫至對等圖形中的每個節點。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-158">Updates a record in the peer graph and then floods the record to each node in the peer graph.</span></span>                                       |
| [<span data-ttu-id="f7bfb-159">**PeerGraphValidateDeferredRecords**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-159">**PeerGraphValidateDeferredRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | <span data-ttu-id="f7bfb-160">向對等圖形基礎結構表示要重新提交任何安全性模組的延遲記錄以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-160">Indicates to the Peer Graphing Infrastructure that it is time to resubmit any deferred records for the security module to validate.</span></span> |



 

## <a name="export-and-import-functions"></a><span data-ttu-id="f7bfb-161">匯出和匯入函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-161">Export and Import Functions</span></span>



| <span data-ttu-id="f7bfb-162">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-162">Function</span></span>                                                   | <span data-ttu-id="f7bfb-163">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-163">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-164">**PeerGraphExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-164">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | <span data-ttu-id="f7bfb-165">將對等圖形資料庫匯出至可移至不同電腦的檔案。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-165">Exports a peer graph database into a file that you can move to a different computer.</span></span> |
| [<span data-ttu-id="f7bfb-166">**PeerGraphImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-166">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | <span data-ttu-id="f7bfb-167">從對等圖形資料庫匯入包含資訊的檔案。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-167">Imports a file that contains the information from a peer graph database.</span></span>             |



 

## <a name="utility-and-support-functions"></a><span data-ttu-id="f7bfb-168">公用程式和支援功能</span><span class="sxs-lookup"><span data-stu-id="f7bfb-168">Utility and Support Functions</span></span>



| <span data-ttu-id="f7bfb-169">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-169">Function</span></span>                                                                     | <span data-ttu-id="f7bfb-170">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-170">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-171">**PeerGraphEndEnumeration**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-171">**PeerGraphEndEnumeration**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | <span data-ttu-id="f7bfb-172">釋放列舉控制碼，並釋出與列舉相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-172">Releases an enumeration handle, and frees the resources associated with an enumeration.</span></span>                                           |
| [<span data-ttu-id="f7bfb-173">**PeerGraphFreeData**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-173">**PeerGraphFreeData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | <span data-ttu-id="f7bfb-174">釋出數個對等圖形 API 函數傳回的資源。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-174">Frees resources that several of the Peer Graphing API functions return.</span></span>                                                           |
| [<span data-ttu-id="f7bfb-175">**PeerGraphGetItemCount**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-175">**PeerGraphGetItemCount**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | <span data-ttu-id="f7bfb-176">捕獲列舉中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-176">Retrieves the number of items in an enumeration.</span></span>                                                                                  |
| [<span data-ttu-id="f7bfb-177">**PeerGraphGetNextItem**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-177">**PeerGraphGetNextItem**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | <span data-ttu-id="f7bfb-178">取得列舉型別中的下一個專案，也就是呼叫特定函式所建立的專案，傳回對等列舉。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-178">Obtains the next item or items in an enumeration created by a call to specific functions, which return a peer enumeration.</span></span>        |
| [<span data-ttu-id="f7bfb-179">**PeerGraphPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-179">**PeerGraphPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | <span data-ttu-id="f7bfb-180">將對等圖表維護的參考時間值轉換為適當的當地語系化時間值，以便顯示在對等電腦上。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-180">Converts the peer graph-maintained reference time value to a localized time value appropriate for display on the peer's computer.</span></span> |
| [<span data-ttu-id="f7bfb-181">**PeerGraphUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-181">**PeerGraphUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | <span data-ttu-id="f7bfb-182">將來自對等電腦的通用時間值轉換為一般對等圖形時間值。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-182">Converts a universal time value from the peer's computer to a common peer graph time value.</span></span>                                       |



 

## <a name="connection-functions"></a><span data-ttu-id="f7bfb-183">連接函數</span><span class="sxs-lookup"><span data-stu-id="f7bfb-183">Connection Functions</span></span>



| <span data-ttu-id="f7bfb-184">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-184">Function</span></span>                                                                 | <span data-ttu-id="f7bfb-185">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-185">Description</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-186">**PeerGraphCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-186">**PeerGraphCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | <span data-ttu-id="f7bfb-187">關閉指定的直接連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-187">Closes a specified direct connection.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="f7bfb-188">**PeerGraphConnect**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-188">**PeerGraphConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | <span data-ttu-id="f7bfb-189">嘗試建立對等圖形中指定節點的連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-189">Attempts to make a connection to a specified node in a peer graph.</span></span> <span data-ttu-id="f7bfb-190">此函數會啟動非同步作業。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-190">This function starts an asynchronous operation.</span></span>                                                                                                                             |
| [<span data-ttu-id="f7bfb-191">**PeerGraphEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-191">**PeerGraphEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | <span data-ttu-id="f7bfb-192">建立並傳回用來列舉本機節點之連接的列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-192">Creates and returns an enumeration handle used to enumerate the connections of a local node.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="f7bfb-193">**PeerGraphOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-193">**PeerGraphOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | <span data-ttu-id="f7bfb-194">允許應用程式與對等圖形中的節點建立直接連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-194">Allows an application to establish a direct connection with a node in a peer graph.</span></span> <span data-ttu-id="f7bfb-195">只有當應用程式所連接的節點已訂閱 **對等 \_ 圖形 \_ 事件 \_ 直接 \_** 線上活動時，才能建立連接。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-195">The connection can only be made if the node to which the application is connecting has subscribed to the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> |
| [<span data-ttu-id="f7bfb-196">**PeerGraphSendData**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-196">**PeerGraphSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | <span data-ttu-id="f7bfb-197">將資料傳送至鄰近節點或直接連接的節點。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-197">Sends data to a neighbor node or a directly connected node.</span></span>                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a><span data-ttu-id="f7bfb-198">事件基礎結構函數</span><span class="sxs-lookup"><span data-stu-id="f7bfb-198">Events Infrastructure Functions</span></span>



| <span data-ttu-id="f7bfb-199">函式</span><span class="sxs-lookup"><span data-stu-id="f7bfb-199">Function</span></span>                                                     | <span data-ttu-id="f7bfb-200">描述</span><span class="sxs-lookup"><span data-stu-id="f7bfb-200">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7bfb-201">**PeerGraphGetEventData**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-201">**PeerGraphGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | <span data-ttu-id="f7bfb-202">抓取對等事件。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-202">Retrieves peer events.</span></span>                                                                                       |
| [<span data-ttu-id="f7bfb-203">**PeerGraphRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-203">**PeerGraphRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | <span data-ttu-id="f7bfb-204">註冊對等圖形和事件種類相關聯之變更的通知對等要求。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-204">Registers a peer's request to be notified of changes associated with a peer graph and event type.</span></span>            |
| [<span data-ttu-id="f7bfb-205">**PeerGraphUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="f7bfb-205">**PeerGraphUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | <span data-ttu-id="f7bfb-206">要求應用程式不會再收到與對等圖表和記錄類型相關聯之變更的通知。</span><span class="sxs-lookup"><span data-stu-id="f7bfb-206">Requests that the application no longer be notified of changes associated with a peer graph and record type.</span></span> |



 

 

 



