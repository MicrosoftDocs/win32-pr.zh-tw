---
title: 應用程式修復和重新開機函式
description: 應用程式復原和重新開機會定義下列功能
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092995"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="c0638-103">應用程式修復和重新開機函式</span><span class="sxs-lookup"><span data-stu-id="c0638-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="c0638-104">應用程式復原和重新開機會定義下列功能：</span><span class="sxs-lookup"><span data-stu-id="c0638-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="c0638-105">函式</span><span class="sxs-lookup"><span data-stu-id="c0638-105">Function</span></span>                                                                               | <span data-ttu-id="c0638-106">描述</span><span class="sxs-lookup"><span data-stu-id="c0638-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0638-107">**ApplicationRecoveryFinished**</span><span class="sxs-lookup"><span data-stu-id="c0638-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="c0638-108">指出呼叫的應用程式已完成其資料復原。</span><span class="sxs-lookup"><span data-stu-id="c0638-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="c0638-109">**ApplicationRecoveryInProgress**</span><span class="sxs-lookup"><span data-stu-id="c0638-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="c0638-110">指出呼叫的應用程式繼續復原資料。</span><span class="sxs-lookup"><span data-stu-id="c0638-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="c0638-111">**GetApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="c0638-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="c0638-112">抓取已針對指定進程註冊之復原回呼常式的指標。</span><span class="sxs-lookup"><span data-stu-id="c0638-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="c0638-113">**GetApplicationRestartSettings**</span><span class="sxs-lookup"><span data-stu-id="c0638-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="c0638-114">抓取為指定進程註冊的重新開機資訊。</span><span class="sxs-lookup"><span data-stu-id="c0638-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="c0638-115">**RegisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="c0638-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="c0638-116">註冊應用程式的使用中實例以進行復原。</span><span class="sxs-lookup"><span data-stu-id="c0638-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="c0638-117">**RegisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="c0638-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="c0638-118">註冊應用程式的使用中實例以重新開機。</span><span class="sxs-lookup"><span data-stu-id="c0638-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="c0638-119">**UnregisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="c0638-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="c0638-120">從復原清單中移除應用程式的使用中實例。</span><span class="sxs-lookup"><span data-stu-id="c0638-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="c0638-121">**UnregisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="c0638-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="c0638-122">從重新開機清單中移除應用程式的使用中實例。</span><span class="sxs-lookup"><span data-stu-id="c0638-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 