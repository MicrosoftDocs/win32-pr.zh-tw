---
title: '電源管理 (TPM 基礎服務) '
description: TBS 會接收電源管理事件。
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "106968882"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="0b3c7-103">電源管理 (TPM 基礎服務) </span><span class="sxs-lookup"><span data-stu-id="0b3c7-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="0b3c7-104">TBS 會接收電源管理事件。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-104">The TBS receives power management events.</span></span> <span data-ttu-id="0b3c7-105">當收到指示時，如果 TPM 或平臺的其他部分即將進入電源狀態，其中的執行將會中斷或 TPM 狀態將會遺失，則 TB 會檢查以判斷目前執行的命令是否可能在系統關機之前完成。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="0b3c7-106">一般來說，TBS 允許 short 和 medium duration 命令完成，但會取消長時間的命令。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="0b3c7-107">傳回命令之後，TBS 會停止將新的命令傳送至 TPM，並為休眠做好準備。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="0b3c7-108">當電源恢復時，TBS 會將命令的結果傳回給呼叫者，然後繼續處理擱置中的 TBS 命令。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="0b3c7-109">TBS 電源管理程式碼會以非同步方式執行，因此即使 TPM 正在處理長命令，也可以處理電源管理要求。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="0b3c7-110">當電腦進入睡眠狀態時，包括 S3 (睡眠) 和 S4 (休眠) 時，TPM 會關閉電源。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="0b3c7-111">因此，所有非持續性 TPM 狀態都會遺失。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="0b3c7-112">進入這些狀態之前，應用程式軟體應該準備好遺失暫時性 TPM 狀態。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="0b3c7-113">當系統從睡眠狀態恢復時，會與 TPM 進行同步處理，讓 [TB] 狀態與 TPM 狀態一致。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="0b3c7-114">應用程式軟體可能需要重新發出中斷的命令。</span><span class="sxs-lookup"><span data-stu-id="0b3c7-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




