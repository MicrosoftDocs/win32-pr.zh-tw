---
title: 排程函數
description: 網路管理排程服務函式會提交及管理特定時間在指定電腦上執行的工作， (或在未來) 的時間。
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967493"
---
# <a name="schedule-functions"></a><span data-ttu-id="9efd2-103">排程函數</span><span class="sxs-lookup"><span data-stu-id="9efd2-103">Schedule Functions</span></span>

<span data-ttu-id="9efd2-104">網路管理排程服務函式會提交及管理特定時間在指定電腦上執行的工作， (或在未來) 的時間。</span><span class="sxs-lookup"><span data-stu-id="9efd2-104">The network management schedule service functions submit and manage jobs that execute on a specified computer at a particular time (or times) in the future.</span></span> <span data-ttu-id="9efd2-105">作業可以包含命令和程式。</span><span class="sxs-lookup"><span data-stu-id="9efd2-105">Jobs can include commands and programs.</span></span> <span data-ttu-id="9efd2-106">如果電腦上的排程服務正在執行，這些函式會管理遠端和本機電腦上的工作。</span><span class="sxs-lookup"><span data-stu-id="9efd2-106">The functions manage jobs at remote and local computers, provided the schedule service is running on the computer.</span></span>

<span data-ttu-id="9efd2-107">排程服務函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="9efd2-107">The schedule service functions are listed following.</span></span>



| <span data-ttu-id="9efd2-108">函式</span><span class="sxs-lookup"><span data-stu-id="9efd2-108">Function</span></span>                                                                     | <span data-ttu-id="9efd2-109">描述</span><span class="sxs-lookup"><span data-stu-id="9efd2-109">Description</span></span>                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9efd2-110">**NetScheduleJobAdd**</span><span class="sxs-lookup"><span data-stu-id="9efd2-110">**NetScheduleJobAdd**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | <span data-ttu-id="9efd2-111">提交工作，以在指定的未來日期和時間執行。</span><span class="sxs-lookup"><span data-stu-id="9efd2-111">Submits a job to run at a specified future date and time.</span></span>        |
| [<span data-ttu-id="9efd2-112">**NetScheduleJobDel**</span><span class="sxs-lookup"><span data-stu-id="9efd2-112">**NetScheduleJobDel**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | <span data-ttu-id="9efd2-113">取消佇列中要在電腦上執行的工作範圍。</span><span class="sxs-lookup"><span data-stu-id="9efd2-113">Cancels a range of jobs queued to run on a computer.</span></span>             |
| [<span data-ttu-id="9efd2-114">**NetScheduleJobEnum**</span><span class="sxs-lookup"><span data-stu-id="9efd2-114">**NetScheduleJobEnum**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | <span data-ttu-id="9efd2-115">列出在指定電腦上佇列的作業。</span><span class="sxs-lookup"><span data-stu-id="9efd2-115">Lists the jobs queued on a specified computer.</span></span>                   |
| [<span data-ttu-id="9efd2-116">**NetScheduleJobGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9efd2-116">**NetScheduleJobGetInfo**</span></span>](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | <span data-ttu-id="9efd2-117">傳回在電腦上佇列的特定作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9efd2-117">Returns information about a particular job queued on a computer.</span></span> |
| [<span data-ttu-id="9efd2-118">**GetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="9efd2-118">**GetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | <span data-ttu-id="9efd2-119">捕獲 AT 服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9efd2-119">Retrieves the AT Service account name.</span></span>                           |
| [<span data-ttu-id="9efd2-120">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="9efd2-120">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | <span data-ttu-id="9efd2-121">設定 AT 服務帳戶名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="9efd2-121">Sets the AT Service account name and password.</span></span>                   |



 

<span data-ttu-id="9efd2-122">若要讓網路管理排程功能成功，呼叫者必須在排程服務執行所在的電腦上具有系統管理員的許可權。</span><span class="sxs-lookup"><span data-stu-id="9efd2-122">For the network management schedule functions to succeed, a caller must have administrator's privilege at the computer where the schedule service is running.</span></span> <span data-ttu-id="9efd2-123">排程服務函式也稱為「作業」和「AT 命令」函數。</span><span class="sxs-lookup"><span data-stu-id="9efd2-123">The schedule service functions are also known as "Job" and "AT command" functions.</span></span> <span data-ttu-id="9efd2-124">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="9efd2-124">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="9efd2-125">[**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)函式會使用 [**AT \_ INFO**](/windows/desktop/api/Lmat/ns-lmat-at_info)結構來指定提交作業時的資訊，以及由 [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)函數來取得已提交之作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9efd2-125">The [**AT\_INFO**](/windows/desktop/api/Lmat/ns-lmat-at_info) structure is used by the [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) function to specify information when submitting a job, and by the [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) function to retrieve information about a job that has been submitted.</span></span> <span data-ttu-id="9efd2-126">[**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)使用 [**AT \_ 列舉**](/windows/desktop/api/Lmat/ns-lmat-at_enum)結構來列舉和傳回已提交工作之整個佇列的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9efd2-126">The [**AT\_ENUM**](/windows/desktop/api/Lmat/ns-lmat-at_enum) structure is used by [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) to enumerate and return information about an entire queue of submitted jobs.</span></span>

 

 