---
description: COMMCONFIG 結構會定義通訊資源的設定，也就是序列或其他方式。
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: 通訊資源設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110701"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="37ed4-103">通訊資源設定</span><span class="sxs-lookup"><span data-stu-id="37ed4-103">Communications Resource Configuration</span></span>

<span data-ttu-id="37ed4-104">[**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig)結構會定義通訊資源的設定，也就是序列或其他方式。</span><span class="sxs-lookup"><span data-stu-id="37ed4-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="37ed4-105">結構的格式會根據 (提供者子類型) 的通訊資源類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="37ed4-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="37ed4-106">前幾個結構成員通用於所有通訊資源;針對特定提供者子類型定義其他成員。</span><span class="sxs-lookup"><span data-stu-id="37ed4-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="37ed4-107">特定服務提供者也可以擴充 **COMMCONFIG** 結構。</span><span class="sxs-lookup"><span data-stu-id="37ed4-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="37ed4-108">應用程式可以使用 [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) 和 [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) 函數來取得和設定通訊資源的設定。</span><span class="sxs-lookup"><span data-stu-id="37ed4-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="37ed4-109">開啟時，會使用其提供者子類型的預設設定來初始化通訊資源。</span><span class="sxs-lookup"><span data-stu-id="37ed4-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="37ed4-110">若要取得並設定提供者子類型的預設設定，請使用 [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) 和 [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) 函數。</span><span class="sxs-lookup"><span data-stu-id="37ed4-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="37ed4-111">若要提示使用者輸入設定資訊，請使用 [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) 函數。</span><span class="sxs-lookup"><span data-stu-id="37ed4-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="37ed4-112">此函式會顯示服務提供者定義的對話方塊，並根據使用者輸入填入 [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) 結構。</span><span class="sxs-lookup"><span data-stu-id="37ed4-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



