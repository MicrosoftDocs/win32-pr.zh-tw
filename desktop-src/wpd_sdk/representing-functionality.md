---
description: 代表功能
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: 代表功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850388"
---
# <a name="representing-functionality"></a><span data-ttu-id="f119e-103">代表功能</span><span class="sxs-lookup"><span data-stu-id="f119e-103">Representing Functionality</span></span>

<span data-ttu-id="f119e-104">功能物件存在，可識別或以邏輯方式將裝置的功能分組。</span><span class="sxs-lookup"><span data-stu-id="f119e-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="f119e-105">例如，應用程式可以藉由尋找 SMS 功能物件，來看到裝置支援 SMS。</span><span class="sxs-lookup"><span data-stu-id="f119e-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="f119e-106">同樣地，應用程式可以藉由尋找靜止的影像捕捉功能物件，來看到裝置具有相機功能。</span><span class="sxs-lookup"><span data-stu-id="f119e-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="f119e-107">這種彈性的物件表示可讓具有多功能功能的裝置輕鬆支援。</span><span class="sxs-lookup"><span data-stu-id="f119e-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="f119e-108">驅動程式可以直接公開任何代表其裝置的功能物件，這比使用傳統裝置類別更細微。</span><span class="sxs-lookup"><span data-stu-id="f119e-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="f119e-109">物件標記法也有助於隔離重迭的功能片段;例如，有些電話可能有兩個相機或四個儲存體。</span><span class="sxs-lookup"><span data-stu-id="f119e-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="f119e-110">在 Windows 7 作業系統中，服務會藉由提供豐富的功能查詢和抽象的內容群組，來擴充功能物件。</span><span class="sxs-lookup"><span data-stu-id="f119e-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="f119e-111">應用程式可以使用服務來探索裝置功能，並更有效率地與內容互動。</span><span class="sxs-lookup"><span data-stu-id="f119e-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="f119e-112">例如，應用程式可以藉由尋找連絡人服務物件，來查看裝置支援連絡人同步處理功能，並可將所有連絡人尋找為服務物件的子物件，而不需要以遞迴方式搜尋儲存體階層。</span><span class="sxs-lookup"><span data-stu-id="f119e-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="f119e-113">服務也允許應用程式在裝置上探索和叫用自訂行為。</span><span class="sxs-lookup"><span data-stu-id="f119e-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f119e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f119e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f119e-115">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="f119e-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



