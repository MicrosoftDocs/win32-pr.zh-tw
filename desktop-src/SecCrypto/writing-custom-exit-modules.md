---
description: 自訂結束模組必須執行由伺服器引擎呼叫的 ICertExit 介面。
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: 撰寫自訂結束模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996908"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="4bfea-103">撰寫自訂結束模組</span><span class="sxs-lookup"><span data-stu-id="4bfea-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="4bfea-104">自訂結束模組必須執行由伺服器引擎呼叫的 [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) 介面。</span><span class="sxs-lookup"><span data-stu-id="4bfea-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="4bfea-105">載入結束模組時，伺服器引擎會呼叫 [**ICertExit：： Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="4bfea-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="4bfea-106">它可讓 exit 模組執行初始化，並傳回值，通知伺服器引擎其需要通知的事件種類。</span><span class="sxs-lookup"><span data-stu-id="4bfea-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="4bfea-107">當伺服器引擎要求時， [**ICertExit：： GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) 方法必須傳回描述字串。</span><span class="sxs-lookup"><span data-stu-id="4bfea-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="4bfea-108">伺服器引擎會呼叫 [**ICertExit：： notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) 方法，以通知結束模組事件已發生。</span><span class="sxs-lookup"><span data-stu-id="4bfea-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="4bfea-109">結束模組可以呼叫 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) 介面，此介面支援許多與 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 介面相同的方法，但 [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 和 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法除外。</span><span class="sxs-lookup"><span data-stu-id="4bfea-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="4bfea-110">如需移除現有的結束模組，以及安裝新的結束模組的相關資訊，請參閱說明中的結束模組自訂主題。</span><span class="sxs-lookup"><span data-stu-id="4bfea-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 



