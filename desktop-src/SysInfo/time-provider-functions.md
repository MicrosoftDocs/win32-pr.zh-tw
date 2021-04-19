---
description: 時間提供者會使用下列函數。
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: 時間提供者函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997869"
---
# <a name="time-provider-functions"></a><span data-ttu-id="d2506-103">時間提供者函數</span><span class="sxs-lookup"><span data-stu-id="d2506-103">Time Provider Functions</span></span>

<span data-ttu-id="d2506-104">時間提供者會使用下列函數。</span><span class="sxs-lookup"><span data-stu-id="d2506-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="d2506-105">函式</span><span class="sxs-lookup"><span data-stu-id="d2506-105">Function</span></span>                                                               | <span data-ttu-id="d2506-106">描述</span><span class="sxs-lookup"><span data-stu-id="d2506-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2506-107">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="d2506-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="d2506-108">通知系統有新的範例可用。</span><span class="sxs-lookup"><span data-stu-id="d2506-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="d2506-109">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="d2506-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="d2506-110">捕獲系統時間狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d2506-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="d2506-111">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="d2506-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="d2506-112">將時間提供者事件記錄在事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="d2506-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="d2506-113">**SetProviderStatusFunc**</span><span class="sxs-lookup"><span data-stu-id="d2506-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="d2506-114">設定時間提供者的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d2506-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="d2506-115">**SetProviderStatusInfoFreeFunc**</span><span class="sxs-lookup"><span data-stu-id="d2506-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="d2506-116">釋放 [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="d2506-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="d2506-117">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="d2506-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="d2506-118">時間提供者管理員呼叫的回呼函式，用來關閉時間提供者。</span><span class="sxs-lookup"><span data-stu-id="d2506-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="d2506-119">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="d2506-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="d2506-120">由時間提供者管理員呼叫的回呼函式，用來將命令傳送給時間提供者。</span><span class="sxs-lookup"><span data-stu-id="d2506-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="d2506-121">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="d2506-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="d2506-122">載入時間提供者 DLL 時，由時間提供者管理員呼叫的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d2506-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



