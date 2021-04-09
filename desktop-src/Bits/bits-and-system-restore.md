---
title: BITS 和系統還原
description: 並非所有 BITS 版本都使用相同的格式來儲存工作。
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020988"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="261d1-103">BITS 和系統還原</span><span class="sxs-lookup"><span data-stu-id="261d1-103">BITS and System Restore</span></span>

<span data-ttu-id="261d1-104">並非所有 BITS 版本都使用相同的格式來儲存工作。</span><span class="sxs-lookup"><span data-stu-id="261d1-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="261d1-105">如果您將電腦還原到 BITS 升級之前的還原點，舊版本的 BITS 可能無法讀取目前的作業資訊。</span><span class="sxs-lookup"><span data-stu-id="261d1-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="261d1-106">如果發生這種情況，BITS 將刪除工作清單並建立新的空白作業清單。</span><span class="sxs-lookup"><span data-stu-id="261d1-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="261d1-107">如此一來，就不會清除與先前的工作清單相關聯的暫存檔案;若要回收磁碟空間，您必須手動刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="261d1-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="261d1-108">熟悉 Windows 命令列的使用者可以使用 [BITSAdmin 工具](bitsadmin-tool.md) 清除 BITS 作業清單，然後執行系統還原，以避免這個問題。</span><span class="sxs-lookup"><span data-stu-id="261d1-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="261d1-109">若要清除 BITS 作業清單，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="261d1-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="261d1-110">**bitsadmin/reset/allusers**</span><span class="sxs-lookup"><span data-stu-id="261d1-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="261d1-111">請注意，您必須具有系統管理員許可權，才能執行此命令。</span><span class="sxs-lookup"><span data-stu-id="261d1-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




