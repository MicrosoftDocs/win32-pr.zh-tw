---
title: RAS 自動撥號
description: 這項功能稱為 \ 0034; 預設連接 \ 0034;已新增至 Windows XP 中的系統。
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- 自動撥號，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968252"
---
# <a name="ras-autodial"></a><span data-ttu-id="64780-104">RAS 自動撥號</span><span class="sxs-lookup"><span data-stu-id="64780-104">RAS AutoDial</span></span>

<span data-ttu-id="64780-105">Windows XP 中的系統已新增稱為「預設連接」的功能。</span><span class="sxs-lookup"><span data-stu-id="64780-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="64780-106">如果連接嘗試失敗，系統會檢查資料庫中是否有 Winsock 名稱或共用名稱) 的明確相符 (。如果沒有，則會撥打預設連接（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="64780-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="64780-107">**Windows 2000：** 當嘗試連線到網路位址失敗，因為無法連線到主機時，自動撥號功能可以自動啟動撥號連線操作。</span><span class="sxs-lookup"><span data-stu-id="64780-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="64780-108">若要這樣做，自動撥號會搜尋其網路位址的資料庫，以找出可用來建立連線的電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="64780-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="64780-109">**Windows NT 4.0：  ** RAS 會保存 Winsock 名稱和/或共用名稱稱的資料庫，當 RAS/VPN 連線為使用中狀態時，您已成功完成。</span><span class="sxs-lookup"><span data-stu-id="64780-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="64780-110">稍後，當 winsock 或共用連線嘗試失敗時，系統會檢查此資料庫，並提供為您撥儲存連接的供應專案。</span><span class="sxs-lookup"><span data-stu-id="64780-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




