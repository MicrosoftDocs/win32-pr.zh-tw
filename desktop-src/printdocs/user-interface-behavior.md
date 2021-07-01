---
description: 請參閱有關檔和列印功能和選項的使用者介面行為討論。
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: 消費者介面行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d007c653ed3f019892e944d9fa4203dc6de11
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119433"
---
# <a name="user-interface-behavior"></a><span data-ttu-id="38901-103">消費者介面行為</span><span class="sxs-lookup"><span data-stu-id="38901-103">User Interface Behavior</span></span>

<span data-ttu-id="38901-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="38901-104">This topic is not current.</span></span> <span data-ttu-id="38901-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="38901-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="38901-106">假設您要建立的 PrintCapabilities 用戶端會讀取 PrintCapabilities 檔，並從每個功能中選取一個或多個選項，並使用這些選項來建立 PrintTicket，以指定要用來處理作業的設定。</span><span class="sxs-lookup"><span data-stu-id="38901-106">Assume that you are creating a PrintCapabilities client that reads in a PrintCapabilities document and selects one or more Options from each Feature and uses those to construct a PrintTicket that specifies the configuration that is to be used to process the Job.</span></span> <span data-ttu-id="38901-107">針對每個感興趣的功能，用戶端必須檢查每個選項，並決定該選項是否適合手邊的工作。</span><span class="sxs-lookup"><span data-stu-id="38901-107">For each Feature of interest, the client must examine each Option, and decide whether that Option is appropriate for the task at hand.</span></span> <span data-ttu-id="38901-108">針對未參數化的選項，可以藉由存取每個 ScoredProperty 的值來進行評估。</span><span class="sxs-lookup"><span data-stu-id="38901-108">For an Option that is not parameterized, it can be evaluated by accessing the Value of each ScoredProperty.</span></span> <span data-ttu-id="38901-109">在 nonparameterized 媒體大小選項的案例中，用戶端會決定每個選項所報告之媒體的寬度和高度維度是否符合所需的維度。</span><span class="sxs-lookup"><span data-stu-id="38901-109">In the case of a nonparameterized media size Option, the client determines whether the width and height dimensions of the media reported in each Option match the dimensions required.</span></span>

<span data-ttu-id="38901-110">在參數化選項的情況下，用戶端必須存取其中一個 ScoredProperty 實例中所包含之 ParameterRef 實例中所指出的 ParameterDef 實例。</span><span class="sxs-lookup"><span data-stu-id="38901-110">In the case of the parameterized Option, the client must access the ParameterDef instance that is indicated in the ParameterRef instance contained in one of the ScoredProperty instances.</span></span> <span data-ttu-id="38901-111">ParameterDef 通常會定義參數所允許的值範圍，以及單位 (英寸、mm 等) 以值表示。</span><span class="sxs-lookup"><span data-stu-id="38901-111">The ParameterDef typically defines the range of values allowed for the parameter, as well as the units (inches, mm, and so on) represented by the value.</span></span> <span data-ttu-id="38901-112">如果必要的維度落在每個參數允許的值範圍內，則用戶端會透過 PrintTicket 中) 的 ParameterInit 實例來初始化參數 (的額外工作。</span><span class="sxs-lookup"><span data-stu-id="38901-112">If the required dimensions fall within the range of values permitted for each of the parameters, the client has the additional task of initializing the parameters (by means of a ParameterInit instance) in the PrintTicket.</span></span> <span data-ttu-id="38901-113">這是特別重要的工作。</span><span class="sxs-lookup"><span data-stu-id="38901-113">This is a particularly important task.</span></span> <span data-ttu-id="38901-114">例如，在不指定媒體的維度的情況下，PrintTicket 不應指定自訂媒體大小，因為產生的 PrintTicket 將會不明確且定義錯誤。</span><span class="sxs-lookup"><span data-stu-id="38901-114">For example, a PrintTicket should not specify a custom media size without specifying the dimensions of the media, because the resulting PrintTicket will be ambiguous and ill-defined.</span></span>

<span data-ttu-id="38901-115">如果用戶端是使用者介面，則必須處理一組類似的情況。</span><span class="sxs-lookup"><span data-stu-id="38901-115">A similar set of circumstances must be handled if the client is a user interface.</span></span> <span data-ttu-id="38901-116">使用者介面通常會顯示針對每個選項所定義的 ScoredProperty 實例值。</span><span class="sxs-lookup"><span data-stu-id="38901-116">The user interface typically displays the values of the ScoredProperty instances defined for each Option.</span></span> <span data-ttu-id="38901-117">為了清楚起見，在參數化選項中顯示參數的允許範圍和單位是很重要的。</span><span class="sxs-lookup"><span data-stu-id="38901-117">For clarity, it is essential to display the allowed range and units for the parameters in a parameterized Option.</span></span> <span data-ttu-id="38901-118">此外，如果使用者選取參數化選項，使用者介面 (UI) 必須提示使用者輸入要用來初始化每個參數的值。</span><span class="sxs-lookup"><span data-stu-id="38901-118">In addition, if the user selects the parameterized Option, the user interface (UI) must prompt the user to enter the value to be used to initialize each parameter.</span></span> <span data-ttu-id="38901-119">最後，UI 必須撰寫可反映所有使用者選取專案的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="38901-119">Finally, the UI must compose a PrintTicket that reflects all of the user's selections.</span></span>

<span data-ttu-id="38901-120">如需 PrintTicket 結構和參數初始化規格的詳細資料，請參閱 [建立 Device-Specific printticket](creating-a-device-specific-printticket.md)。</span><span class="sxs-lookup"><span data-stu-id="38901-120">For the details of PrintTicket construction and specification of parameter initialization, see [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span> <span data-ttu-id="38901-121">如需有關 ParameterRef 實例的取值以及解讀 ParameterDef 實例的詳細資訊，請參閱 [使用參數](using-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="38901-121">For information about dereferencing ParameterRef instances and interpreting ParameterDef instances, see [Using Parameters](using-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="38901-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="38901-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38901-123">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="38901-123">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



