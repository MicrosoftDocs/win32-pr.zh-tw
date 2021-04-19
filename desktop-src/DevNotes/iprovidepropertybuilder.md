---
description: 在實 IProvidePropertyBuilder 介面時，會允許物件指定屬性的屬性產生器物件。
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: IProvidePropertyBuilder 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990518"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="ed004-103">IProvidePropertyBuilder 介面</span><span class="sxs-lookup"><span data-stu-id="ed004-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="ed004-104">在實 **IProvidePropertyBuilder** 介面時，會允許物件指定屬性的屬性產生器物件。</span><span class="sxs-lookup"><span data-stu-id="ed004-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="ed004-105">在 \[ \] 按下按鈕時，會在 Microsoft Visual Studio 的屬性瀏覽器上 (...) 的省略號按鈕叫用產生器，並透過 [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) 叫用。</span><span class="sxs-lookup"><span data-stu-id="ed004-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="ed004-106">若要為指定的屬性提供建立器，請針對 [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md)的目前屬性，傳回應叫用的屬性產生器 GUID。</span><span class="sxs-lookup"><span data-stu-id="ed004-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="ed004-107">產生器通常會透過強制回應對話方塊來實行。</span><span class="sxs-lookup"><span data-stu-id="ed004-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="ed004-108">這個介面的版本是1.0。</span><span class="sxs-lookup"><span data-stu-id="ed004-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="ed004-109">方法呼叫會在動態指派的端點上收到 (如 MSMQ 二進位檔案中的端點對應) 所述，並使用 UUID (全域唯一識別碼) "33C0C1D8-33CF-11d3-BFF2-00C04F990235"。</span><span class="sxs-lookup"><span data-stu-id="ed004-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="ed004-110">成員</span><span class="sxs-lookup"><span data-stu-id="ed004-110">Members</span></span>

<span data-ttu-id="ed004-111">**IProvidePropertyBuilder： iunknown** 介面繼承自 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ed004-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ed004-112">**IProvidePropertyBuilder** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ed004-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="ed004-113">方法</span><span class="sxs-lookup"><span data-stu-id="ed004-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ed004-114">方法</span><span class="sxs-lookup"><span data-stu-id="ed004-114">Methods</span></span>

<span data-ttu-id="ed004-115">**IProvidePropertyBuilder： IUnknown** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ed004-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="ed004-116">方法</span><span class="sxs-lookup"><span data-stu-id="ed004-116">Method</span></span>                                                                       | <span data-ttu-id="ed004-117">描述</span><span class="sxs-lookup"><span data-stu-id="ed004-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed004-118">**ExecuteBuilder**</span><span class="sxs-lookup"><span data-stu-id="ed004-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="ed004-119">通知物件應針對指定的屬性顯示其產生器。</span><span class="sxs-lookup"><span data-stu-id="ed004-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="ed004-120">**MapPropertyToBuilder**</span><span class="sxs-lookup"><span data-stu-id="ed004-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="ed004-121">檢查產生器是否應該與特定屬性相關聯。</span><span class="sxs-lookup"><span data-stu-id="ed004-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="ed004-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed004-122">Requirements</span></span>



| <span data-ttu-id="ed004-123">需求</span><span class="sxs-lookup"><span data-stu-id="ed004-123">Requirement</span></span> | <span data-ttu-id="ed004-124">值</span><span class="sxs-lookup"><span data-stu-id="ed004-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed004-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ed004-125">DLL</span></span><br/> | <dl> <span data-ttu-id="ed004-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed004-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
