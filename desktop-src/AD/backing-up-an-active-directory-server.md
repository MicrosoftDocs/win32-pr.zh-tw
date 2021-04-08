---
title: 備份 Active Directory 伺服器
description: Active Directory 伺服器備份需要您備份資料庫和交易記錄。 本主題提供備份應用程式如何備份 Active Directory 目錄服務的逐步解說。
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- 備份 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020749"
---
# <a name="backing-up-an-active-directory-server"></a><span data-ttu-id="63051-105">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="63051-105">Backing Up an Active Directory Server</span></span>

<span data-ttu-id="63051-106">Active Directory 伺服器備份需要您備份資料庫和交易記錄。</span><span class="sxs-lookup"><span data-stu-id="63051-106">An Active Directory server backup requires you to back up the database and the transaction logs.</span></span> <span data-ttu-id="63051-107">本主題提供備份應用程式如何備份 Active Directory 目錄服務的逐步解說。</span><span class="sxs-lookup"><span data-stu-id="63051-107">This topic provides a walkthrough of how a backup application backs up the Active Directory directory service.</span></span>

<span data-ttu-id="63051-108">這些備份函式的呼叫者必須擁有 **SE \_ 備份 \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="63051-108">The caller of these backup functions must have the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="63051-109">您可以使用 [**DsSetAuthIdentity**](dssetauthidentity.md) 函數來設定用來呼叫目錄備份/還原功能的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="63051-109">You can use the [**DsSetAuthIdentity**](dssetauthidentity.md) function to set the security context under which the directory backup/restore functions are called.</span></span>

<span data-ttu-id="63051-110">**若要備份 Active Directory 伺服器，請執行下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="63051-110">**To backup an Active Directory server, perform the following steps**</span></span>

1.  <span data-ttu-id="63051-111">呼叫 [**DsIsNTDSOnline**](dsisntdsonline.md) 函數來判斷 Active Directory Domain Services 是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="63051-111">Call the [**DsIsNTDSOnline**](dsisntdsonline.md) function to determine if Active Directory Domain Services are running.</span></span>
2.  <span data-ttu-id="63051-112">如果 Active Directory Domain Services 正在執行，請呼叫 [**DsBackupPrepare**](dsbackupprepare.md) 函數來初始化備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="63051-112">If Active Directory Domain Services are running, call the [**DsBackupPrepare**](dsbackupprepare.md) function to initialize a backup context handle.</span></span> <span data-ttu-id="63051-113">如果 Active Directory Domain Services 未執行，則無法備份，且備份應用程式必須讓備份作業失敗。</span><span class="sxs-lookup"><span data-stu-id="63051-113">If Active Directory Domain Services are not running, it cannot be backed up and the backup application must fail the backup operation.</span></span>
3.  <span data-ttu-id="63051-114">呼叫 [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) 函數，以取得要備份的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="63051-114">Call the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function to get a list of files to back up.</span></span> <span data-ttu-id="63051-115">若要釋放此函式所傳回的記憶體，請呼叫 [**DsBackupFree**](dsbackupfree.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="63051-115">To release the memory returned by this function, call the [**DsBackupFree**](dsbackupfree.md) function.</span></span>
4.  <span data-ttu-id="63051-116">針對傳回的檔案清單中的每個名稱，呼叫 [**DsBackupOpenFile**](dsbackupopenfile.md) 函式，然後重複呼叫 [**DsBackupRead**](dsbackupread.md) 函式，直到讀取整個檔案為止。</span><span class="sxs-lookup"><span data-stu-id="63051-116">For each name in the returned list of files, call the [**DsBackupOpenFile**](dsbackupopenfile.md) function followed by repeated calls to the [**DsBackupRead**](dsbackupread.md) function until the entire file has been read.</span></span> <span data-ttu-id="63051-117">當您完成讀取檔案時，請呼叫 [**DsBackupClose**](dsbackupclose.md) 函式來關閉它。</span><span class="sxs-lookup"><span data-stu-id="63051-117">When you have finished reading the file, call the [**DsBackupClose**](dsbackupclose.md) function to close it.</span></span>
5.  <span data-ttu-id="63051-118">備份所有資料庫檔案之後，請呼叫 [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) 函數來取得交易記錄檔的清單。</span><span class="sxs-lookup"><span data-stu-id="63051-118">After all database files are backed up, call the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function to get a list of transaction logs.</span></span> <span data-ttu-id="63051-119">此清單的處理方式就和資料庫檔案清單一樣。</span><span class="sxs-lookup"><span data-stu-id="63051-119">This list is handled just like the list of database files.</span></span>
6.  <span data-ttu-id="63051-120">當您完成交易記錄的備份時，請呼叫 [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) 函數來刪除已備份的所有已認可交易記錄。</span><span class="sxs-lookup"><span data-stu-id="63051-120">When you have finished backing up the transaction log, call the [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) function to delete all committed transaction logs that were backed up.</span></span>
7.  <span data-ttu-id="63051-121">儲存 [**DsBackupPrepare**](dsbackupprepare.md) 函式所提供的到期權杖內容。</span><span class="sxs-lookup"><span data-stu-id="63051-121">Save the contents of the expiry token provided by the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span> <span data-ttu-id="63051-122">這可儲存在檔案或其他的持續性記憶體中。</span><span class="sxs-lookup"><span data-stu-id="63051-122">This can be saved in a file or some other persistent memory.</span></span> <span data-ttu-id="63051-123">此權杖必須傳遞至 [**DsRestorePrepare**](dsrestoreprepare.md) 函式，才能起始還原作業。</span><span class="sxs-lookup"><span data-stu-id="63051-123">This token must be passed to the [**DsRestorePrepare**](dsrestoreprepare.md) function to initiate a restore operation.</span></span>
8.  <span data-ttu-id="63051-124">將權杖指標傳遞至 [**DsBackupFree**](dsbackupfree.md) 函式，以釋放到期權杖的記憶體。</span><span class="sxs-lookup"><span data-stu-id="63051-124">Free the memory for the expiry token by passing the token pointer to the [**DsBackupFree**](dsbackupfree.md) function.</span></span>
9.  <span data-ttu-id="63051-125">最後，呼叫 [**DsBackupEnd**](dsbackupend.md) 函式，以釋放與備份內容控制碼相關聯的所有資源。</span><span class="sxs-lookup"><span data-stu-id="63051-125">Finally, call the [**DsBackupEnd**](dsbackupend.md) function to release all resources associated with the backup context handle.</span></span>

 

 




