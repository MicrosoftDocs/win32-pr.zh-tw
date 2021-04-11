---
description: 摘要資訊資料流程包含可透過 Microsoft Windows 檔案總管查看之封裝的相關資訊。
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: 關於摘要資訊資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115393"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="a31c3-103">關於摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="a31c3-103">About the Summary Information Stream</span></span>

<span data-ttu-id="a31c3-104">摘要資訊資料流程包含可透過 Microsoft Windows 檔案總管查看之封裝的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a31c3-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="a31c3-105">這項資訊可透過 **IStream** 介面進行存取。</span><span class="sxs-lookup"><span data-stu-id="a31c3-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="a31c3-106">這是由作者提供，以提供每個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a31c3-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="a31c3-107">摘要資訊資料流程會使用 COM 來提供資料庫的結構化儲存體。</span><span class="sxs-lookup"><span data-stu-id="a31c3-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="a31c3-108">COM 支援透過 **IStream** 介面存取結構化儲存體的概念。</span><span class="sxs-lookup"><span data-stu-id="a31c3-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="a31c3-109">結構化儲存體可支援屬性集的概念，做為將幾乎任何資訊序列化的彈性方法。</span><span class="sxs-lookup"><span data-stu-id="a31c3-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="a31c3-110">COM 規格定義了單一標準屬性集，也就是用來填入可從 Windows 檔案總管查看的屬性工作表的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="a31c3-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="a31c3-111">因此，當使用者以滑鼠右鍵按一下安裝程式資料庫或轉換，然後選取 [ [屬性](about-properties.md)] 時，就可以看到儲存在摘要資訊資料流程中的資訊。</span><span class="sxs-lookup"><span data-stu-id="a31c3-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="a31c3-112">如需摘要屬性集的清單，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="a31c3-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="a31c3-113">如需與資料庫、轉換和修補程式搭配使用之摘要資訊屬性的簡短說明，請參閱 [摘要屬性描述](summary-property-descriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="a31c3-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



