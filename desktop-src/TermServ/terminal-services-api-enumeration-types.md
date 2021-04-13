---
title: 遠端桌面服務 API 列舉類型
description: 列出搭配遠端桌面服務 API 使用的列舉類型。
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301183"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="d11e9-103">遠端桌面服務 API 列舉類型</span><span class="sxs-lookup"><span data-stu-id="d11e9-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="d11e9-104">下列列舉類型會與遠端桌面服務 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d11e9-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d11e9-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="d11e9-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d11e9-106">**WTS \_ CONFIG \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="d11e9-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="d11e9-107">包含值，這些值表示在呼叫 [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) 和 [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) 函數時要設定或抓取的使用者設定資訊類型。</span><span class="sxs-lookup"><span data-stu-id="d11e9-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-108">**WTS \_ CONFIG \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="d11e9-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="d11e9-109">指定 [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) 函數所傳回的設定資訊來源。</span><span class="sxs-lookup"><span data-stu-id="d11e9-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-110">**WTS \_ CONNECTSTATE \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="d11e9-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="d11e9-111">指定遠端桌面服務會話的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="d11e9-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-112">**WTS \_ 資訊 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="d11e9-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="d11e9-113">包含值，這些值表示在呼叫 [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) 函式時要取出的會話資訊類型。</span><span class="sxs-lookup"><span data-stu-id="d11e9-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-114">**WTS \_ 型別 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="d11e9-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="d11e9-115">指定遠端桌面服務函數已在緩衝區中傳回的結構類型。</span><span class="sxs-lookup"><span data-stu-id="d11e9-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-116">**WTS \_ 虛擬 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="d11e9-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="d11e9-117">包含值，這些值表示要取出的虛擬通道資訊類型。</span><span class="sxs-lookup"><span data-stu-id="d11e9-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-118">**WTSSBX \_ 位址 \_ 系列**</span><span class="sxs-lookup"><span data-stu-id="d11e9-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="d11e9-119">包含值，這些值表示用於重新導向之網路位址的位址系列。</span><span class="sxs-lookup"><span data-stu-id="d11e9-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-120">**WTSSBX \_ 機器 \_ 清空**</span><span class="sxs-lookup"><span data-stu-id="d11e9-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="d11e9-121">包含值，指出遠端桌面工作階段主機 (RD 工作階段主機) server 的清空狀態。</span><span class="sxs-lookup"><span data-stu-id="d11e9-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-122">**WTSSBX \_ 機器 \_ 會話 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d11e9-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="d11e9-123">包含值，指出 RD 工作階段主機伺服器的會話模式。</span><span class="sxs-lookup"><span data-stu-id="d11e9-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-124">**WTSSBX \_ 電腦 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d11e9-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="d11e9-125">包含表示伺服器目前狀態的值。</span><span class="sxs-lookup"><span data-stu-id="d11e9-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-126">**WTSSBX \_ 通知 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d11e9-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="d11e9-127">包含值，指出 RD 工作階段主機伺服器或使用者會話上發生的狀態變更類型。</span><span class="sxs-lookup"><span data-stu-id="d11e9-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="d11e9-128">**WTSSBX \_ 會話 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d11e9-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="d11e9-129">包含值，這些值表示使用者會話的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="d11e9-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




