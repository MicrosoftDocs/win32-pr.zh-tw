---
title: 壓縮和解壓縮設定
description: 壓縮和解壓縮設定
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，設定壓縮機
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，設定壓縮機
- ICM_CONFIGURE 訊息
- ICQueryConfigure 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932140"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="eeec4-107">壓縮和解壓縮設定</span><span class="sxs-lookup"><span data-stu-id="eeec4-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="eeec4-108">您的應用程式可以自動設定壓縮程式或解壓縮程式，也可以允許使用者進行設定。</span><span class="sxs-lookup"><span data-stu-id="eeec4-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="eeec4-109">如果可行，可讓使用者設定壓縮程式或解壓縮程式;這可讓您不考慮壓縮程式或解壓縮程式的所有選項。</span><span class="sxs-lookup"><span data-stu-id="eeec4-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="eeec4-110">使用者可以使用 [設定] 對話方塊來設定 [壓縮程式] 或 [解壓縮程式]。</span><span class="sxs-lookup"><span data-stu-id="eeec4-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="eeec4-111">您可以將 [**ICM \_ 設定**](icm-configure.md) 訊息傳送至 bc-vcm-lvm-hyperv (或使用 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) 宏) 來判斷壓縮或解壓縮是否可顯示 [設定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eeec4-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="eeec4-112">若是如此，請傳送 ICM \_ 設定訊息 (或使用 [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) 宏) 來顯示它。</span><span class="sxs-lookup"><span data-stu-id="eeec4-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="eeec4-113">您的應用程式可以 [**傳送 \_ icm >getstate**](icm-getstate.md) 和 [**icm \_ SETSTATE**](icm-setstate.md) 訊息 (或使用 [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)、 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)和 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) 宏) 來取得和設定壓縮程式或解壓縮程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="eeec4-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="eeec4-114">如果您的應用程式建立或修改狀態，則必須先取得壓縮程式或解壓縮程式資料的配置，再還原其狀態。</span><span class="sxs-lookup"><span data-stu-id="eeec4-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="eeec4-115">或者，如果您的應用程式從壓縮程式或解壓縮程式取得狀態，並在後續的會話中使用它來還原狀態，則必須確保它只會還原從目前正在使用的壓縮程式或解壓縮程式取得的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="eeec4-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




