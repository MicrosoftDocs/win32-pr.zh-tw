---
description: 下列函式用於網路 DDE。
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: 網路 DDE 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981698"
---
# <a name="network-dde-functions"></a><span data-ttu-id="ec2af-103">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="ec2af-103">Network DDE Functions</span></span>

<span data-ttu-id="ec2af-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="ec2af-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="ec2af-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="ec2af-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="ec2af-106">下列函式用於網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="ec2af-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="ec2af-107">函式</span><span class="sxs-lookup"><span data-stu-id="ec2af-107">Function</span></span>                                                   | <span data-ttu-id="ec2af-108">描述</span><span class="sxs-lookup"><span data-stu-id="ec2af-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec2af-109">**NDdeGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="ec2af-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="ec2af-110">將網路 DDE 函數所傳回的錯誤碼轉換成錯誤字串，以說明傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ec2af-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="ec2af-111">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="ec2af-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="ec2af-112">抓取與 DDE 共用相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="ec2af-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="ec2af-113">**NDdeGetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="ec2af-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="ec2af-114">抓取與在伺服器使用者的受信任共用清單中之 DDE 共用相關聯的選項。</span><span class="sxs-lookup"><span data-stu-id="ec2af-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="ec2af-115">**NDdeIsValidAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="ec2af-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="ec2af-116">判斷應用程式和主題字串 ( "*AppName* \| *TopicName*" ) 是否使用適當的語法。</span><span class="sxs-lookup"><span data-stu-id="ec2af-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="ec2af-117">**NDdeIsValidShareName**</span><span class="sxs-lookup"><span data-stu-id="ec2af-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="ec2af-118">判斷共用名稱是否使用適當的語法。</span><span class="sxs-lookup"><span data-stu-id="ec2af-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="ec2af-119">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="ec2af-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="ec2af-120">設定與 DDE 共用相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="ec2af-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="ec2af-121">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="ec2af-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="ec2af-122">在目前使用者的內容中，授與指定的 DDE 共用信任狀態。</span><span class="sxs-lookup"><span data-stu-id="ec2af-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="ec2af-123">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="ec2af-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="ec2af-124">建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。</span><span class="sxs-lookup"><span data-stu-id="ec2af-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="ec2af-125">**NDdeShareDel**</span><span class="sxs-lookup"><span data-stu-id="ec2af-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="ec2af-126">從 DSDM 中刪除 DDE 共用。</span><span class="sxs-lookup"><span data-stu-id="ec2af-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="ec2af-127">**NDdeShareEnum**</span><span class="sxs-lookup"><span data-stu-id="ec2af-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="ec2af-128">抓取可用的 DDE 共用清單。</span><span class="sxs-lookup"><span data-stu-id="ec2af-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="ec2af-129">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="ec2af-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="ec2af-130">捕獲 DDE 共用資訊。</span><span class="sxs-lookup"><span data-stu-id="ec2af-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="ec2af-131">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="ec2af-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="ec2af-132">設定 DDE 共用資訊。</span><span class="sxs-lookup"><span data-stu-id="ec2af-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="ec2af-133">**NDdeTrustedShareEnum**</span><span class="sxs-lookup"><span data-stu-id="ec2af-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="ec2af-134">抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2af-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



