---
title: 操作外掛程式方法
description: 操作外掛程式方法
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931790"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="e49da-103">操作外掛程式方法</span><span class="sxs-lookup"><span data-stu-id="e49da-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="e49da-104">所有作業外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="e49da-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="e49da-105">某些回呼機制會呼叫多次，直到報告所有結果為止。</span><span class="sxs-lookup"><span data-stu-id="e49da-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="e49da-106">下表提供操作回呼方法的總覽。</span><span class="sxs-lookup"><span data-stu-id="e49da-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="e49da-107">方法</span><span class="sxs-lookup"><span data-stu-id="e49da-107">Method</span></span>                                                                         | <span data-ttu-id="e49da-108">描述</span><span class="sxs-lookup"><span data-stu-id="e49da-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e49da-109">**WSManPluginFreeRequestDetails**</span><span class="sxs-lookup"><span data-stu-id="e49da-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="e49da-110">釋放配置給 [**WSMAN \_ 外掛程式 \_ 要求**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) 結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e49da-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="e49da-111">**WSManPluginGetOperationParameters**</span><span class="sxs-lookup"><span data-stu-id="e49da-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="e49da-112">取得操作資訊，例如與作業相關聯的超時時間和資料限制。</span><span class="sxs-lookup"><span data-stu-id="e49da-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="e49da-113">**WSManPluginOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="e49da-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="e49da-114">記錄作業的完成。</span><span class="sxs-lookup"><span data-stu-id="e49da-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="e49da-115">**WSManPluginReceiveResult**</span><span class="sxs-lookup"><span data-stu-id="e49da-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="e49da-116">將結果報告給 Windows 遠端管理 (WinRM) 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e49da-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="e49da-117">**WSManPluginReportCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e49da-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="e49da-118">將 shell 和命令內容回報給 WinRM 基礎結構，以便可以針對 shell 和/或命令執行進一步的作業。</span><span class="sxs-lookup"><span data-stu-id="e49da-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




