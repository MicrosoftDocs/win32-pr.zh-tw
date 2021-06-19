---
description: 瞭解如何建立一般的 PrintTicket，以防裝置的 PrintCapabilities 檔無法使用。
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: 建立一般的 PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e611205663138b9cc3c0d3cd315c2c19d2d7e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409521"
---
# <a name="creating-a-generic-printticket"></a><span data-ttu-id="ffab6-103">建立一般的 PrintTicket</span><span class="sxs-lookup"><span data-stu-id="ffab6-103">Creating a Generic PrintTicket</span></span>

<span data-ttu-id="ffab6-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ffab6-104">This topic is not current.</span></span> <span data-ttu-id="ffab6-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ffab6-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ffab6-106">如果裝置的 PrintCapabilities 檔無法使用，或目標裝置不明，您應該建立一般的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="ffab6-106">If the PrintCapabilities document for the device is unavailable, or if the target device is unknown, you should construct a generic PrintTicket.</span></span> <span data-ttu-id="ffab6-107">因為沒有提供一組功能和選項專案的 PrintCapabilities 檔，或參數，所以必須直接從 Print Schema 關鍵字取得這些元素類型支援的實例。</span><span class="sxs-lookup"><span data-stu-id="ffab6-107">Because there is no PrintCapabilities document that provides a set of Feature and Option elements, or parameters, the supported instances of these element types must be obtained directly from the Print Schema Keywords.</span></span>

<span data-ttu-id="ffab6-108">當您建立一般 PrintTicket 時，應使用下列清單中所示的步驟。</span><span class="sxs-lookup"><span data-stu-id="ffab6-108">The steps shown in the following list should be used when you create a generic PrintTicket.</span></span>

1.  <span data-ttu-id="ffab6-109">建立空白的 XML 檔，其中包含 PrintTicket 根。</span><span class="sxs-lookup"><span data-stu-id="ffab6-109">Create an empty XML document that contains the PrintTicket root.</span></span> <span data-ttu-id="ffab6-110">將命名空間前置詞指派給列印架構命名空間。</span><span class="sxs-lookup"><span data-stu-id="ffab6-110">Assign a namespace prefix to the Print Schema namespace.</span></span> <span data-ttu-id="ffab6-111">指定架構版本。</span><span class="sxs-lookup"><span data-stu-id="ffab6-111">Specify the Schema version.</span></span>

2.  <span data-ttu-id="ffab6-112">檢查 Print Schema 關鍵字中的功能實例，並決定您要在您的 PrintTicket 中定義哪些。</span><span class="sxs-lookup"><span data-stu-id="ffab6-112">Examine the Feature instances in the Print Schema Keywords and determine which of these you want defined in your PrintTicket.</span></span> <span data-ttu-id="ffab6-113">將這些功能實例加入至您的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="ffab6-113">Add these Feature instances to your PrintTicket.</span></span> <span data-ttu-id="ffab6-114">當您傳輸 subfeature 時，您必須傳送父功能，並保留在 PrintTicket 中的功能與 subfeature 之間的父子式關聯性。</span><span class="sxs-lookup"><span data-stu-id="ffab6-114">When you transfer a subfeature, you must transfer the parent Feature, and preserve the parent-child relationship between the Feature and subfeature in the PrintTicket.</span></span>

    <span data-ttu-id="ffab6-115">針對您傳送的每個功能實例，判斷哪些選項實例適用于您的 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="ffab6-115">For each Feature instance that you transfer, determine which Option instances are applicable to your PrintTicket.</span></span> <span data-ttu-id="ffab6-116">從這組選項實例，將每個整個選項實例都傳送在列印架構中，然後移除任何存在的屬性實例，但對於您的 PrintTicket 具有重要性的可能例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ffab6-116">From this set of Option instances, transfer each entire Option instance as it appears in the Print Schema, and then remove any Property instances that are present, with the possible exception of those that have significance to your PrintTicket.</span></span> <span data-ttu-id="ffab6-117">保留所有 ScoredProperty 實例，並確定您保留其位置;它們是選項定義的內建部分。</span><span class="sxs-lookup"><span data-stu-id="ffab6-117">Keep all of the ScoredProperty instances, making sure that you preserve their location; they are an intrinsic part of the Option definition.</span></span>

3.  <span data-ttu-id="ffab6-118">您也可以將屬性實例新增至任何 ScoredProperty。</span><span class="sxs-lookup"><span data-stu-id="ffab6-118">You may also add Property instances to any ScoredProperty.</span></span> <span data-ttu-id="ffab6-119">只有當 PrintTicket 提供者明確支援其使用時，屬性元素才適用。</span><span class="sxs-lookup"><span data-stu-id="ffab6-119">Property elements are applicable only if the PrintTicket provider explicitly supports their use.</span></span> <span data-ttu-id="ffab6-120">每個提供者都應記錄所有支援之屬性實例的用途和用法。</span><span class="sxs-lookup"><span data-stu-id="ffab6-120">Each provider should document the purpose and use of all supported Property instances.</span></span> <span data-ttu-id="ffab6-121">因為您不知道哪個提供者將處理 PrintTicket，所以您可能只想附加系統 PrintTicket 提供者明確支援的屬性實例。</span><span class="sxs-lookup"><span data-stu-id="ffab6-121">Because you have no idea which provider will process the PrintTicket, you might wish to append only the Property instances that are explicitly supported by the system PrintTicket provider.</span></span>

4.  <span data-ttu-id="ffab6-122">如果 Print Schema 關鍵字將特定功能的 SelectionType 屬性設定為 PickMany，您可以為該功能選取一個以上的選項，但前提是指定為 IdentityOption 的選項不是選取的選項之一。</span><span class="sxs-lookup"><span data-stu-id="ffab6-122">If the Print Schema Keywords set the SelectionType Property to PickMany for a particular Feature, you may select more than one Option for that Feature, provided that the Option designated as IdentityOption is not one of those selected.</span></span> <span data-ttu-id="ffab6-123">列印架構中的 IdentityOption 與 Postscript PPD 檔案和 Unidrv GPD 檔案中的 [無] 選項有相同的效果;它是一種無作業的服務。</span><span class="sxs-lookup"><span data-stu-id="ffab6-123">IdentityOption in the Print Schema has the same effect as the None option in Postscript PPD files and Unidrv GPD files; it serves as a no-op.</span></span>

5.  <span data-ttu-id="ffab6-124">檢查 ParameterDef 實例的列印架構關鍵字，這些實例應該在您的 PrintTicket 中初始化。</span><span class="sxs-lookup"><span data-stu-id="ffab6-124">Examine the Print Schema Keywords for ParameterDef instances that should be initialized in your PrintTicket.</span></span> <span data-ttu-id="ffab6-125">針對每個這類 ParameterDef 實例，選取要在 PrintTicket 的 ParameterInit 實例中使用的值。</span><span class="sxs-lookup"><span data-stu-id="ffab6-125">For each such ParameterDef instance, select the Value to be used in the ParameterInit instance in the PrintTicket.</span></span> <span data-ttu-id="ffab6-126">這個值必須是正確的資料類型、必須落在 ParameterDef 實例中定義的範圍內，而且必須符合 ParameterDef 實例中指定的所有其他需求。</span><span class="sxs-lookup"><span data-stu-id="ffab6-126">This Value must be of the correct data type, must fall within the range defined in the ParameterDef instance, and must meet all of the other requirements specified in the ParameterDef instance.</span></span> <span data-ttu-id="ffab6-127">使用 ParameterInit 實例將參數初始化為您所選取的值。</span><span class="sxs-lookup"><span data-stu-id="ffab6-127">Use a ParameterInit instance to initialize the parameter to the Value you have selected.</span></span>

    <span data-ttu-id="ffab6-128">如果您要 (UI) 元件開發使用者介面，請設計您的 PrintTicket 產生方法，讓使用者可以輸入 ParameterInit 元素的值。</span><span class="sxs-lookup"><span data-stu-id="ffab6-128">If you are developing a user interface (UI) component, design your PrintTicket generation methods so that users can enter the Value for the ParameterInit element.</span></span> <span data-ttu-id="ffab6-129">此外，UI 輸入方法應該觀察並符合相關聯 ParameterDef 專案所指定的任何輸入限制。</span><span class="sxs-lookup"><span data-stu-id="ffab6-129">In addition, the UI entry method should observe and comply with any input restrictions specified by the associated ParameterDef element.</span></span>

6.  <span data-ttu-id="ffab6-130">檢查在 PrintTicket 中出現 ParameterRef 的每個選項實例的內容。</span><span class="sxs-lookup"><span data-stu-id="ffab6-130">Examine the contents of each Option instance that appears in the PrintTicket for occurrences of ParameterRef.</span></span> <span data-ttu-id="ffab6-131">如果對應的 ParameterInit 實例尚未出現在 PrintTicket 中，請依照上一個步驟在 PrintTicket 中建立 ParameterInit 實例。</span><span class="sxs-lookup"><span data-stu-id="ffab6-131">If a corresponding ParameterInit instance does not already appear in the PrintTicket, follow the previous step to create a ParameterInit instance in the PrintTicket.</span></span> <span data-ttu-id="ffab6-132">這個 ParameterInit 實例的目的是要初始化 ParameterRef 實例所參考的參數。</span><span class="sxs-lookup"><span data-stu-id="ffab6-132">The purpose of this ParameterInit instance is to initialize the parameter referenced by the ParameterRef instance.</span></span>

7.  <span data-ttu-id="ffab6-133">請記住，處理作業的裝置可能不支援 PrintTicket 中指定的每項功能。</span><span class="sxs-lookup"><span data-stu-id="ffab6-133">Keep in mind that the device that processes the job might not support every Feature specified in the PrintTicket.</span></span> <span data-ttu-id="ffab6-134">也請記住，可能會支援已命名的功能，但該功能的指定選項可能不會。</span><span class="sxs-lookup"><span data-stu-id="ffab6-134">Keep in mind also, that a named Feature might be supported, but a specified Option of that Feature might not be.</span></span> <span data-ttu-id="ffab6-135">相同的警告適用于參數。</span><span class="sxs-lookup"><span data-stu-id="ffab6-135">The same caveats apply to parameters.</span></span> <span data-ttu-id="ffab6-136">即使裝置支援具名引數，在 ParameterInit 實例中指定的值可能不在裝置的有效範圍內。</span><span class="sxs-lookup"><span data-stu-id="ffab6-136">Even if a device supports a named parameter, the Value specified in the ParameterInit instance might not be within the valid range for the device.</span></span>

8.  <span data-ttu-id="ffab6-137">檢查必須存在於您的 PrintTicket 中之屬性實例的列印架構關鍵字。</span><span class="sxs-lookup"><span data-stu-id="ffab6-137">Examine the Print Schema Keywords for Property instances that must be present in your PrintTicket.</span></span> <span data-ttu-id="ffab6-138">將每個屬性的屬性實例加入至您的 PrintTicket，並使用 Value 元素類型為其提供適當的值。</span><span class="sxs-lookup"><span data-stu-id="ffab6-138">Add a Property instance for each of these to your PrintTicket, and provide a suitable value for it using the Value element type.</span></span> <span data-ttu-id="ffab6-139">請確定屬性實例正確地放在 PrintTicket 內。</span><span class="sxs-lookup"><span data-stu-id="ffab6-139">Make sure that Property instances are located properly within the PrintTicket.</span></span> <span data-ttu-id="ffab6-140">請確定您查閱了 PrintTicket 架構，而不是 PrintCapabilities 架構。</span><span class="sxs-lookup"><span data-stu-id="ffab6-140">Make sure that you consult the PrintTicket Schema rather than the PrintCapabilities Schema.</span></span>

9.  <span data-ttu-id="ffab6-141">檢查 PrintTicket 架構中定義的選擇性屬性實例。</span><span class="sxs-lookup"><span data-stu-id="ffab6-141">Examine the optional Property instances defined in the PrintTicket Schema.</span></span> <span data-ttu-id="ffab6-142">如果您的 PrintTicket 中有任何這類屬性實例，請在您的 PrintTicket 中建立它們。</span><span class="sxs-lookup"><span data-stu-id="ffab6-142">If there are any such Property instances that should be in your PrintTicket, create them in your PrintTicket.</span></span>

10. <span data-ttu-id="ffab6-143">相同專案類型的子系不可嵌套至超過10個元素的深度。</span><span class="sxs-lookup"><span data-stu-id="ffab6-143">Children of the same element type may not nest to a depth of more than 10 elements.</span></span> <span data-ttu-id="ffab6-144">這項規則會獨立套用到每個可定義的元素類型。</span><span class="sxs-lookup"><span data-stu-id="ffab6-144">This rule applies independently to each type of element that can be defined.</span></span>

> [!Note]  
> <span data-ttu-id="ffab6-145">必須使用 UTF-8 或 UTF-16 來編碼 PrintTicket XML 內容。</span><span class="sxs-lookup"><span data-stu-id="ffab6-145">PrintTicket XML content MUST be encoded using either UTF-8 or UTF-16.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ffab6-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffab6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffab6-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ffab6-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



