---
title: 裝置設定空間
description: 裝置的設定空間是所有可能值的集合，可指派給裝置的所有屬性。
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4871da3695e81168d43504456c357b0cf566b7f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409481"
---
# <a name="device-configuration-space-and-device-configurations"></a><span data-ttu-id="9fd23-103">裝置設定空間和裝置設定</span><span class="sxs-lookup"><span data-stu-id="9fd23-103">Device Configuration Space and Device Configurations</span></span>

<span data-ttu-id="9fd23-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9fd23-104">This topic is not current.</span></span> <span data-ttu-id="9fd23-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9fd23-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9fd23-106">裝置的設定 *空間* 是所有可能值的集合，可指派給裝置的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="9fd23-106">A device's *configuration space* is the set of all possible values that can be assigned to all of the attributes of the device.</span></span> <span data-ttu-id="9fd23-107">在 PrintCapabilities 中描述裝置設定空間的兩個最重要的原因如下所示。</span><span class="sxs-lookup"><span data-stu-id="9fd23-107">The two most important reasons to describe the configuration space of the device in the PrintCapabilities are as follows.</span></span>

1.  <span data-ttu-id="9fd23-108">這項資訊可大幅提升對裝置功能的瞭解。</span><span class="sxs-lookup"><span data-stu-id="9fd23-108">The information contributes significantly to an increased understanding of the device's capabilities.</span></span> <span data-ttu-id="9fd23-109">這項資訊可讓 PrintCapabilities 的用戶端輕鬆地產生使用者介面 (UI) 元素，讓使用者更容易選取特定的設定來處理作業。</span><span class="sxs-lookup"><span data-stu-id="9fd23-109">This information makes it easier for a client of the PrintCapabilities to generate user interface (UI) elements, which makes it easier for the end user to select a particular configuration to process a job.</span></span> <span data-ttu-id="9fd23-110">藉由提供應用程式的更多詳細資料，以及最終使用者的功能，使用者的列印意圖可以更有效率地完成。</span><span class="sxs-lookup"><span data-stu-id="9fd23-110">By providing more details of the device's capabilities to the application and ultimately to the end user, the user's printing intent can be more effectively fulfilled.</span></span>

2.  <span data-ttu-id="9fd23-111">PrintCapabilities 中顯示的某些裝置屬性可能會取決於用戶端選取的特定設定。</span><span class="sxs-lookup"><span data-stu-id="9fd23-111">Certain device properties presented in the PrintCapabilities might be dependent on the particular configuration selected by the client.</span></span>

<span data-ttu-id="9fd23-112">部分資訊不應併入 PrintCapabilities 中。</span><span class="sxs-lookup"><span data-stu-id="9fd23-112">Some information should not be incorporated into the PrintCapabilities.</span></span> <span data-ttu-id="9fd23-113">這包含的資訊不會影響作業的建立方式、不會限制建立作業的方式，也不會影響裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="9fd23-113">This includes information that does not affect the way a job is created, does not impose constraints on the way a job is created, nor otherwise affects the device properties.</span></span> <span data-ttu-id="9fd23-114">例如，裝置可能會報告狀態資訊，例如等待處理的作業集合。</span><span class="sxs-lookup"><span data-stu-id="9fd23-114">For example, a device might be able to report status information, such as the set of jobs waiting to be processed.</span></span> <span data-ttu-id="9fd23-115">這項資訊不會影響格式化作業所需的資訊，也不會提供裝置中可用功能的任何指示。</span><span class="sxs-lookup"><span data-stu-id="9fd23-115">This information has no effect on the information needed to format the job, nor does it provide any indication of the capabilities available in the device.</span></span> <span data-ttu-id="9fd23-116">基於這個理由，PrintCapabilities 中不需要有這種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="9fd23-116">For this reason, this type of information does not need to be present in the PrintCapabilities.</span></span>

## <a name="device-constraints"></a><span data-ttu-id="9fd23-117">裝置條件約束</span><span class="sxs-lookup"><span data-stu-id="9fd23-117">Device Constraints</span></span>

<span data-ttu-id="9fd23-118">由於裝置上的條件約束，許多裝置不支援設定空間中的所有可能設定。</span><span class="sxs-lookup"><span data-stu-id="9fd23-118">Many devices do not support all possible configurations in the configuration space due to a constraint on the device.</span></span> <span data-ttu-id="9fd23-119">例如，裝置可能會受到限制，無法在透明媒體上執行雙工列印。</span><span class="sxs-lookup"><span data-stu-id="9fd23-119">For example, a device can be constrained from performing duplex printing on transparent media.</span></span> <span data-ttu-id="9fd23-120">條件約束可代表實體限制：某些媒體類型的內容太過嚴格，無法流經裝置中的特定紙張路徑，因此不能放在某些輸入位置或路由傳送至某些輸出的位置。目前，PrintCapabilities 或 PrintTicket 提供者必須負責驗證輸入 PrintTicket 所代表的設定，以確認它不代表不正確設定。</span><span class="sxs-lookup"><span data-stu-id="9fd23-120">A constraint can represent a physical limitation: some media types are simply too rigid to travel through certain paper paths in the device, and so cannot be placed in some input slots or be routed to some output bins. Currently it is the responsibility of the PrintCapabilities or PrintTicket provider to validate the configuration represented by the input PrintTicket, to verify that it does not represent an invalid configuration.</span></span> <span data-ttu-id="9fd23-121">如果設定無效，PrintCapabilities 或 PrintTicket 提供者應該以使設定變成有效的方式修改設定。</span><span class="sxs-lookup"><span data-stu-id="9fd23-121">If the configuration is invalid, the PrintCapabilities or PrintTicket provider should modify the configuration in such a way that it becomes valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fd23-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fd23-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd23-123">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9fd23-123">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



