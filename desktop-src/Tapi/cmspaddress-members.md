---
description: 下列清單包含 CMSP 位址成員。
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: CMSPAddress 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853084"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="87075-103">CMSPAddress 成員</span><span class="sxs-lookup"><span data-stu-id="87075-103">CMSPAddress Members</span></span>



| <span data-ttu-id="87075-104">成員類型</span><span class="sxs-lookup"><span data-stu-id="87075-104">Member types</span></span>                    | <span data-ttu-id="87075-105">Name</span><span class="sxs-lookup"><span data-stu-id="87075-105">Name</span></span>                    | <span data-ttu-id="87075-106">描述</span><span class="sxs-lookup"><span data-stu-id="87075-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87075-107">Iunknown</span><span class="sxs-lookup"><span data-stu-id="87075-107">Iunknown</span></span>                        | <span data-ttu-id="87075-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="87075-108">\*m\_pFTM</span></span>               | <span data-ttu-id="87075-109">無限制執行緒封送處理器的指標。</span><span class="sxs-lookup"><span data-stu-id="87075-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="87075-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="87075-110">HANDLE</span></span>                          | <span data-ttu-id="87075-111">m \_ htEvent</span><span class="sxs-lookup"><span data-stu-id="87075-111">m\_htEvent</span></span>              | <span data-ttu-id="87075-112">Tapi3.dll 的事件的控制碼，可用來通知 TAPI 要將資料傳送給它。</span><span class="sxs-lookup"><span data-stu-id="87075-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="87075-113">清單 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="87075-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="87075-114">m \_ EventList</span><span class="sxs-lookup"><span data-stu-id="87075-114">m\_EventList</span></span>            | <span data-ttu-id="87075-115">事件的清單。</span><span class="sxs-lookup"><span data-stu-id="87075-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="87075-116">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="87075-116">CMSPCritSection</span></span>                 | <span data-ttu-id="87075-117">m \_ EventDataLock</span><span class="sxs-lookup"><span data-stu-id="87075-117">m\_EventDataLock</span></span>        | <span data-ttu-id="87075-118">使用 TAPI 保護與事件處理相關之資料的鎖定。</span><span class="sxs-lookup"><span data-stu-id="87075-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="87075-119">ITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="87075-119">ITTerminalManager</span></span>               | <span data-ttu-id="87075-120">\*m \_ pITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="87075-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="87075-121">終端機管理員物件的指標。</span><span class="sxs-lookup"><span data-stu-id="87075-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="87075-122">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="87075-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="87075-123">m \_ 終端機</span><span class="sxs-lookup"><span data-stu-id="87075-123">m\_Terminals</span></span>            | <span data-ttu-id="87075-124">可以在位址上使用的靜態終端機清單。</span><span class="sxs-lookup"><span data-stu-id="87075-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="87075-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="87075-125">BOOL</span></span>                            | <span data-ttu-id="87075-126">m \_ fTerminalsUpToDate</span><span class="sxs-lookup"><span data-stu-id="87075-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="87075-127">如果終端機清單是最新的，則此旗標為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="87075-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="87075-128">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="87075-128">CMSPCritSection</span></span>                 | <span data-ttu-id="87075-129">m \_ TerminalDataLock</span><span class="sxs-lookup"><span data-stu-id="87075-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="87075-130">保護終端機相關資料成員的鎖定。</span><span class="sxs-lookup"><span data-stu-id="87075-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



