---
description: 下列主題描述應用程式如何使用系統登錄提供者來提供您所建立之類別的資料。
ms.assetid: 84604fbc-50b2-410d-84bf-4a408be26ee2
ms.tgt_platform: multiple
title: 使用系統登錄提供者進行程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c31563a7a4ef22f1de7c4c697b201ff998a73c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848390"
---
# <a name="programming-with-the-system-registry-provider"></a><span data-ttu-id="a13fa-103">使用系統登錄提供者進行程式設計</span><span class="sxs-lookup"><span data-stu-id="a13fa-103">Programming with the System Registry Provider</span></span>

<span data-ttu-id="a13fa-104">下列主題描述應用程式如何使用系統登錄提供者來提供您所建立之類別的資料。</span><span class="sxs-lookup"><span data-stu-id="a13fa-104">The following topics describe how applications can use the System Registry Provider to provide data for classes that you create.</span></span>



| <span data-ttu-id="a13fa-105">主題</span><span class="sxs-lookup"><span data-stu-id="a13fa-105">Topic</span></span>                                                                                                                      | <span data-ttu-id="a13fa-106">描述</span><span class="sxs-lookup"><span data-stu-id="a13fa-106">Description</span></span>                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a13fa-107">定義 System Registry 提供者的類別</span><span class="sxs-lookup"><span data-stu-id="a13fa-107">Defining Classes for the System Registry Provider</span></span>](defining-classes-for-the-system-registry-provider.md)                 | <span data-ttu-id="a13fa-108">若要存取系統登錄，您必須建立將登錄資訊儲存在 Windows Management Instrumentation (WMI) 存放庫中的 Windows 類別。</span><span class="sxs-lookup"><span data-stu-id="a13fa-108">To access the system registry, you must create Windows classes that store registry information in the Windows Management Instrumentation (WMI) repository.</span></span>                                                                     |
| [<span data-ttu-id="a13fa-109">使用系統登錄提供者作為屬性提供者</span><span class="sxs-lookup"><span data-stu-id="a13fa-109">Using the System Registry Provider as a Property Provider</span></span>](using-the-system-registry-provider-as-a-property-provider.md) | <span data-ttu-id="a13fa-110">系統登錄提供者會要求您使用數個限定詞來查看登錄屬性。</span><span class="sxs-lookup"><span data-stu-id="a13fa-110">The System Registry Provider requires that you use several qualifiers to view registry properties.</span></span>                                                                                                                             |
| [<span data-ttu-id="a13fa-111">描述登錄的資源</span><span class="sxs-lookup"><span data-stu-id="a13fa-111">Describing a Resource for the Registry</span></span>](describing-a-resource-for-the-registry.md)                                       | <span data-ttu-id="a13fa-112">您可以存取登錄中描述系統資源的資料。</span><span class="sxs-lookup"><span data-stu-id="a13fa-112">You can access data in the registry that describes a system resource.</span></span> <span data-ttu-id="a13fa-113">若要修改資訊，系統登錄提供者需要特定的語法。</span><span class="sxs-lookup"><span data-stu-id="a13fa-113">To modify the information, the System Registry Provider requires a specific syntax.</span></span>                                                                      |
| [<span data-ttu-id="a13fa-114">存取未命名的登錄值</span><span class="sxs-lookup"><span data-stu-id="a13fa-114">Accessing an Unnamed Registry Value</span></span>](accessing-an-unnamed-registry-value.md)                                             | <span data-ttu-id="a13fa-115">若要存取大部分的登錄值，請建立一個類別來接收 WMI 中的值，或者您可以檢查特定的登錄屬性。</span><span class="sxs-lookup"><span data-stu-id="a13fa-115">To access most registry values, create a class to receive the values in WMI, or you can examine specific registry properties.</span></span> <span data-ttu-id="a13fa-116">不過，系統登錄提供者需要特殊的語法來查看未命名的登錄值。</span><span class="sxs-lookup"><span data-stu-id="a13fa-116">However, the System Registry Provider requires a special syntax to view unnamed registry values.</span></span> |



 

 

 



