---
title: Windows 事件記錄檔工具
description: Windows 事件記錄檔提供下列用來建立提供者的工具。
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374884"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="7e5cf-103">Windows 事件記錄檔工具</span><span class="sxs-lookup"><span data-stu-id="7e5cf-103">Windows Event Log Tools</span></span>

<span data-ttu-id="7e5cf-104">Windows 事件記錄檔提供下列用來建立提供者的工具。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="7e5cf-105">工具</span><span class="sxs-lookup"><span data-stu-id="7e5cf-105">Tool</span></span>                                                           | <span data-ttu-id="7e5cf-106">描述</span><span class="sxs-lookup"><span data-stu-id="7e5cf-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e5cf-107">**訊息編譯器 (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="7e5cf-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="7e5cf-108">用來編譯檢測資訊清單和訊息文字檔的命令列公用程式。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="7e5cf-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="7e5cf-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="7e5cf-110">一種命令列公用程式，主要是用來在電腦上註冊您的提供者。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="7e5cf-111">您也可以使用它來取得提供者的中繼資料資訊、其事件，以及記錄事件的通道，以及從通道或記錄檔查詢事件。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="7e5cf-112">WevtUtil.exe 工具組含在% windir% System32 中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="7e5cf-113">如需使用資訊，請輸入 "wevtutil/？"</span><span class="sxs-lookup"><span data-stu-id="7e5cf-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="7e5cf-114">。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-114">at a command prompt.</span></span><br/> <span data-ttu-id="7e5cf-115">此命令僅限於系統管理員群組的成員，且必須以較高的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="7e5cf-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
