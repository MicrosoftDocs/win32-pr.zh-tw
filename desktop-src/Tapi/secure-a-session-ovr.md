---
description: 如果應用程式不想讓來自 TAPI 或服務提供者的會話外來事件產生任何干擾，它應該保護呼叫的安全。
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: 保護會話的安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991373"
---
# <a name="secure-a-session"></a><span data-ttu-id="38392-103">保護會話的安全</span><span class="sxs-lookup"><span data-stu-id="38392-103">Secure a Session</span></span>

<span data-ttu-id="38392-104">如果應用程式不想讓來自 TAPI 或服務提供者的會話外來事件產生任何干擾，它應該保護呼叫的安全。</span><span class="sxs-lookup"><span data-stu-id="38392-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="38392-105">例如，在類比環境通話等候的聲場中，可以在原始電話上終結傳真或數據機會話。</span><span class="sxs-lookup"><span data-stu-id="38392-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="38392-106">應用程式可以在呼叫進行時或在呼叫已經存在時，保護呼叫的安全。</span><span class="sxs-lookup"><span data-stu-id="38392-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="38392-107">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="38392-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="38392-108">**TAPI 2.x：** 請參閱 [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall)。</span><span class="sxs-lookup"><span data-stu-id="38392-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="38392-109">**TAPI 3.x：** 請參閱 [**ITAddress：： Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward)。</span><span class="sxs-lookup"><span data-stu-id="38392-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
