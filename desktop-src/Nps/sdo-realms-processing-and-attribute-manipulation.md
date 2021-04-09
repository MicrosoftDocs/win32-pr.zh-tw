---
title: 領域處理和屬性操作
description: 領域處理（也稱為屬性操作）是指將要求存取權的使用者名稱轉換。
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682674"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="1e811-103">領域處理和屬性操作</span><span class="sxs-lookup"><span data-stu-id="1e811-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="1e811-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="1e811-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1e811-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="1e811-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1e811-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="1e811-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1e811-107">領域處理（也稱為屬性操作）是指將要求存取權的使用者名稱轉換。</span><span class="sxs-lookup"><span data-stu-id="1e811-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="1e811-108">也可以操作呼叫端識別碼和被呼叫的工作站識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e811-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="1e811-109">領域處理規則是 Proxy 配置檔案屬性集合的一部分。</span><span class="sxs-lookup"><span data-stu-id="1e811-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="1e811-110">針對每個操作，您需要建立兩個 [操作規則](/windows/desktop/Nps/sdo-manipulation-rule) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1e811-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="1e811-111">每個屬性都是一個字串值。</span><span class="sxs-lookup"><span data-stu-id="1e811-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="1e811-112">第一個規則包含表示要比對之模式的正則運算式。</span><span class="sxs-lookup"><span data-stu-id="1e811-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="1e811-113">第二個規則包含表示取代文字的正則運算式。</span><span class="sxs-lookup"><span data-stu-id="1e811-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="1e811-114">您也必須建立 [操作目標](/windows/desktop/Nps/sdo-manipulation-target) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1e811-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="1e811-115">這個屬性是一個列舉，可指定要操作的使用者資訊部分。</span><span class="sxs-lookup"><span data-stu-id="1e811-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="1e811-116">建立屬性的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="1e811-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="1e811-117">NPS 會依照這些屬性的建立順序來處理它們。</span><span class="sxs-lookup"><span data-stu-id="1e811-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="1e811-118">下表顯示一組操作屬性的範例。</span><span class="sxs-lookup"><span data-stu-id="1e811-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="1e811-119">名稱</span><span class="sxs-lookup"><span data-stu-id="1e811-119">Name</span></span>                 | <span data-ttu-id="1e811-120">類型</span><span class="sxs-lookup"><span data-stu-id="1e811-120">Type</span></span>         | <span data-ttu-id="1e811-121">字串值</span><span class="sxs-lookup"><span data-stu-id="1e811-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="1e811-122">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="1e811-122">msManipulationRule</span></span>   | <span data-ttu-id="1e811-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e811-123">**VT\_BSTR**</span></span> | <span data-ttu-id="1e811-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="1e811-124">"@company.com"</span></span>   |
| <span data-ttu-id="1e811-125">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="1e811-125">msManipulationRule</span></span>   | <span data-ttu-id="1e811-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e811-126">**VT\_BSTR**</span></span> | <span data-ttu-id="1e811-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="1e811-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="1e811-128">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="1e811-128">msManipulationRule</span></span>   | <span data-ttu-id="1e811-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e811-129">**VT\_BSTR**</span></span> | <span data-ttu-id="1e811-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="1e811-130">"^.+@"</span></span>           |
| <span data-ttu-id="1e811-131">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="1e811-131">msManipulationRule</span></span>   | <span data-ttu-id="1e811-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="1e811-132">**VT\_BSTR**</span></span> | <span data-ttu-id="1e811-133">"guest@"</span><span class="sxs-lookup"><span data-stu-id="1e811-133">"guest@"</span></span>         |
| <span data-ttu-id="1e811-134">msManipulationTarget</span><span class="sxs-lookup"><span data-stu-id="1e811-134">msManipulationTarget</span></span> | <span data-ttu-id="1e811-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="1e811-135">**VT\_I4**</span></span>   | <span data-ttu-id="1e811-136">「1」</span><span class="sxs-lookup"><span data-stu-id="1e811-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="1e811-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e811-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e811-138">物件模型階層</span><span class="sxs-lookup"><span data-stu-id="1e811-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="1e811-139">SDO 支援的屬性</span><span class="sxs-lookup"><span data-stu-id="1e811-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="1e811-140">建立連接要求原則</span><span class="sxs-lookup"><span data-stu-id="1e811-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="1e811-141">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="1e811-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="1e811-142">**ISdoDictionaryOld**</span><span class="sxs-lookup"><span data-stu-id="1e811-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="1e811-143">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="1e811-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 