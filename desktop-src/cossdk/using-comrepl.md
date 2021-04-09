---
description: 使用 COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: 使用 COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688996"
---
# <a name="using-comrepl"></a><span data-ttu-id="98b80-103">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="98b80-103">Using COMREPL</span></span>

<span data-ttu-id="98b80-104">若要啟動 COMREPL 命令列公用程式，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="98b80-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="98b80-105">\\ \\ 在命令提示字元中輸入下列命令，將% windir% system32 Com 新增至預設環境路徑：</span><span class="sxs-lookup"><span data-stu-id="98b80-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="98b80-106">**set path =% PATH%;% windir% \\ system32 \\ Com**</span><span class="sxs-lookup"><span data-stu-id="98b80-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="98b80-107">輸入下列 COMREPL 命令：</span><span class="sxs-lookup"><span data-stu-id="98b80-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="98b80-108">**COMREPL** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="98b80-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="98b80-109">其中：</span><span class="sxs-lookup"><span data-stu-id="98b80-109">where:</span></span>

    -   <span data-ttu-id="98b80-110">*sourceComputer* 是來源的電腦名稱稱</span><span class="sxs-lookup"><span data-stu-id="98b80-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="98b80-111">*targetComputerList* 是以空格分隔的目標電腦名稱稱</span><span class="sxs-lookup"><span data-stu-id="98b80-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="98b80-112">**/n** 在開始複寫之前隱藏確認提示</span><span class="sxs-lookup"><span data-stu-id="98b80-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="98b80-113">**/v** 將記錄檔輸出回顯至主控台</span><span class="sxs-lookup"><span data-stu-id="98b80-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="98b80-114">備註</span><span class="sxs-lookup"><span data-stu-id="98b80-114">Notes</span></span>

-   <span data-ttu-id="98b80-115">由於 COM + 不會複寫 (只有設定資料和應用程式) ，所有目的電腦都必須已安裝 COM +。</span><span class="sxs-lookup"><span data-stu-id="98b80-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="98b80-116">使用者必須在來源和目的電腦上通過系統應用程式的角色檢查。</span><span class="sxs-lookup"><span data-stu-id="98b80-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="98b80-117">不會複寫角色可使用的本機電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="98b80-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="98b80-118">目的電腦 (s) 必須在線上。</span><span class="sxs-lookup"><span data-stu-id="98b80-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="98b80-119">使用者必須負責複寫所有非 COM + 資料 (例如，資料庫資料表、資料檔案等等，) 到目的電腦 (s) 。</span><span class="sxs-lookup"><span data-stu-id="98b80-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="98b80-120">叢集可以參與複寫，但請注意，COMREPL 只會複寫到已命名的電腦。</span><span class="sxs-lookup"><span data-stu-id="98b80-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98b80-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="98b80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98b80-122">檔案管理</span><span class="sxs-lookup"><span data-stu-id="98b80-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="98b80-123">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="98b80-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="98b80-124">複寫階段</span><span class="sxs-lookup"><span data-stu-id="98b80-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="98b80-125">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="98b80-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



