---
description: PHONEPRIVILEGE \_ 位旗標常數描述可開啟手機裝置的各種方式。
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: 'PHONEPRIVILEGE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995110"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="e7ee4-103">PHONEPRIVILEGE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="e7ee4-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="e7ee4-104">**PHONEPRIVILEGE \_** 位旗標常數描述可開啟手機裝置的各種方式。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="e7ee4-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE \_ 監視**</span><span class="sxs-lookup"><span data-stu-id="e7ee4-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7ee4-106">使用 [監視] 許可權開啟手機裝置的應用程式，會收到關於電話上發生的事件和狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="e7ee4-107">應用程式無法在手機裝置上叫用會變更其狀態的任何作業，因此只能叫用狀態作業。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="e7ee4-108">多個應用程式可以在任何指定時間監視電話裝置。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7ee4-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="e7ee4-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7ee4-110">使用「擁有者」許可權開啟手機裝置的應用程式，可以變更手機的燈、響鈴、顯示、hookswitch 和資料區塊的狀態。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="e7ee4-111">在 [擁有者] 模式中開啟手機裝置也會提供電話裝置的監視。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="e7ee4-112">在任何指定的時間，都只允許一個應用程式成為電話裝置的擁有者。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ee4-113">備註</span><span class="sxs-lookup"><span data-stu-id="e7ee4-113">Remarks</span></span>

<span data-ttu-id="e7ee4-114">無延伸。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-114">No extensibility.</span></span> <span data-ttu-id="e7ee4-115">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="e7ee4-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ee4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7ee4-116">Requirements</span></span>



| <span data-ttu-id="e7ee4-117">需求</span><span class="sxs-lookup"><span data-stu-id="e7ee4-117">Requirement</span></span> | <span data-ttu-id="e7ee4-118">值</span><span class="sxs-lookup"><span data-stu-id="e7ee4-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e7ee4-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e7ee4-119">TAPI version</span></span><br/> | <span data-ttu-id="e7ee4-120">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e7ee4-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e7ee4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e7ee4-121">Header</span></span><br/>       | <dl> <span data-ttu-id="e7ee4-122"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e7ee4-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




