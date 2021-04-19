---
description: 建立篩選屬性頁
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: 建立篩選屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106976998"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="42297-103">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="42297-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="42297-104">本節說明如何使用 [**CBasePropertyPage**](cbasepropertypage.md) 類別，建立自訂 DirectShow 篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="42297-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="42297-105">本節中的範例程式碼會顯示建立屬性頁所需的所有步驟。</span><span class="sxs-lookup"><span data-stu-id="42297-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="42297-106">此範例會顯示可支援飽和度屬性之假設性影片效果篩選的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="42297-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="42297-107">屬性頁有一個滑杆，可讓使用者移動以調整篩選的飽和度層級。</span><span class="sxs-lookup"><span data-stu-id="42297-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="42297-108">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="42297-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="42297-109">步驟1。定義用來設定屬性的機制</span><span class="sxs-lookup"><span data-stu-id="42297-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="42297-110">步驟2。執行 ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="42297-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="42297-111">步驟3。支援 QueryInterface</span><span class="sxs-lookup"><span data-stu-id="42297-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="42297-112">步驟4：建立屬性頁</span><span class="sxs-lookup"><span data-stu-id="42297-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="42297-113">步驟5。將指標儲存至篩選</span><span class="sxs-lookup"><span data-stu-id="42297-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="42297-114">步驟6：初始化對話方塊</span><span class="sxs-lookup"><span data-stu-id="42297-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="42297-115">步驟7：處理視窗訊息</span><span class="sxs-lookup"><span data-stu-id="42297-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="42297-116">步驟8。套用屬性變更</span><span class="sxs-lookup"><span data-stu-id="42297-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="42297-117">步驟9。中斷屬性頁面的連線</span><span class="sxs-lookup"><span data-stu-id="42297-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="42297-118">步驟10。支援 COM 註冊</span><span class="sxs-lookup"><span data-stu-id="42297-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="42297-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="42297-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42297-120">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="42297-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



