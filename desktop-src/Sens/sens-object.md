---
description: 系統事件通知服務 (SENS) 將 SENS coclass 定義為 SENS 類型程式庫的一部分。
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: SENS 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975853"
---
# <a name="sens-object"></a><span data-ttu-id="7bb57-103">SENS 物件</span><span class="sxs-lookup"><span data-stu-id="7bb57-103">SENS Object</span></span>

<span data-ttu-id="7bb57-104">系統事件通知服務 (SENS) 將 SENS coclass 定義為 SENS 類型程式庫的一部分。</span><span class="sxs-lookup"><span data-stu-id="7bb57-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="7bb57-105">實作</span><span class="sxs-lookup"><span data-stu-id="7bb57-105">Implementation</span></span>

<span data-ttu-id="7bb57-106">SENS 物件的執行是由作業系統提供。</span><span class="sxs-lookup"><span data-stu-id="7bb57-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="7bb57-107">建立/存取函式</span><span class="sxs-lookup"><span data-stu-id="7bb57-107">Creation/Access Functions</span></span>



| <span data-ttu-id="7bb57-108">函式</span><span class="sxs-lookup"><span data-stu-id="7bb57-108">Function</span></span>                                      | <span data-ttu-id="7bb57-109">描述</span><span class="sxs-lookup"><span data-stu-id="7bb57-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="7bb57-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7bb57-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="7bb57-111">使用 CLSID 來建立 SENS 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="7bb57-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="7bb57-112">介面</span><span class="sxs-lookup"><span data-stu-id="7bb57-112">Interfaces</span></span>



| <span data-ttu-id="7bb57-113">介面</span><span class="sxs-lookup"><span data-stu-id="7bb57-113">Interface</span></span>                            | <span data-ttu-id="7bb57-114">描述</span><span class="sxs-lookup"><span data-stu-id="7bb57-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bb57-115">**IsensNetwork**</span><span class="sxs-lookup"><span data-stu-id="7bb57-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="7bb57-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="7bb57-116">Default.</span></span> <span data-ttu-id="7bb57-117">訂閱者應用程式中接收物件所執行的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="7bb57-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="7bb57-118">**IsensOnNow**</span><span class="sxs-lookup"><span data-stu-id="7bb57-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="7bb57-119">訂閱者應用程式中接收物件所執行的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="7bb57-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="7bb57-120">**IsensLogon**</span><span class="sxs-lookup"><span data-stu-id="7bb57-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="7bb57-121">訂閱者應用程式中接收物件所執行的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="7bb57-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="7bb57-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="7bb57-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="7bb57-123">訂閱者應用程式中接收物件所執行的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="7bb57-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="7bb57-124">適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7bb57-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7bb57-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bb57-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb57-126">**ISensLogon**</span><span class="sxs-lookup"><span data-stu-id="7bb57-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="7bb57-127">**ISensNetwork**</span><span class="sxs-lookup"><span data-stu-id="7bb57-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="7bb57-128">**ISensOnNow**</span><span class="sxs-lookup"><span data-stu-id="7bb57-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="7bb57-129">關於系統事件通知服務</span><span class="sxs-lookup"><span data-stu-id="7bb57-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
