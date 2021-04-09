---
description: 定義要執行之裝置的製造商和型號中繼資料。 此元素僅用於 (主機) 的裝置執行。
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: thisModelMetadata 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851484"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="5060d-104">thisModelMetadata 元素</span><span class="sxs-lookup"><span data-stu-id="5060d-104">thisModelMetadata element</span></span>

<span data-ttu-id="5060d-105">定義要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5060d-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="5060d-106">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="5060d-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="5060d-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="5060d-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="5060d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="5060d-108">Attributes</span></span>

<span data-ttu-id="5060d-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="5060d-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5060d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5060d-110">Child elements</span></span>



| <span data-ttu-id="5060d-111">元素</span><span class="sxs-lookup"><span data-stu-id="5060d-111">Element</span></span>                                                     | <span data-ttu-id="5060d-112">描述</span><span class="sxs-lookup"><span data-stu-id="5060d-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5060d-113">**製造商**</span><span class="sxs-lookup"><span data-stu-id="5060d-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="5060d-114">製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="5060d-114">Name of the manufacturer.</span></span> <span data-ttu-id="5060d-115">中繼資料中至少必須有一個 [**製造商**](manufacturer.md) 或 [**manufacturerLS**](manufacturerls.md) 。</span><span class="sxs-lookup"><span data-stu-id="5060d-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="5060d-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="5060d-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="5060d-117">製造商名稱的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="5060d-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="5060d-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="5060d-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="5060d-119">製造商 URL 位址。</span><span class="sxs-lookup"><span data-stu-id="5060d-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="5060d-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="5060d-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="5060d-121">裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5060d-121">Name of the device.</span></span> <span data-ttu-id="5060d-122">中繼資料中至少必須有一個 [**modelName**](modelname.md) 或 [**modelNameLS**](modelnamels.md) 。</span><span class="sxs-lookup"><span data-stu-id="5060d-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="5060d-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="5060d-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="5060d-124">裝置名稱的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="5060d-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="5060d-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="5060d-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="5060d-126">裝置的型號。</span><span class="sxs-lookup"><span data-stu-id="5060d-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="5060d-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="5060d-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="5060d-128">裝置型號的 URL 位址。</span><span class="sxs-lookup"><span data-stu-id="5060d-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="5060d-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="5060d-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="5060d-130">裝置所屬的 PnP-X 類別。</span><span class="sxs-lookup"><span data-stu-id="5060d-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="5060d-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="5060d-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="5060d-132">裝置型號呈現資料的 URL 位址。</span><span class="sxs-lookup"><span data-stu-id="5060d-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="5060d-133">子項目順序</span><span class="sxs-lookup"><span data-stu-id="5060d-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="5060d-134">父元素</span><span class="sxs-lookup"><span data-stu-id="5060d-134">Parent elements</span></span>



| <span data-ttu-id="5060d-135">元素</span><span class="sxs-lookup"><span data-stu-id="5060d-135">Element</span></span>                                     | <span data-ttu-id="5060d-136">描述</span><span class="sxs-lookup"><span data-stu-id="5060d-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5060d-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="5060d-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="5060d-138">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="5060d-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5060d-139">備註</span><span class="sxs-lookup"><span data-stu-id="5060d-139">Remarks</span></span>

<span data-ttu-id="5060d-140">製造商中繼資料符合裝置設定檔中所述的製造商中繼資料區段 (如需詳細資訊，請參閱裝置設定檔) 。</span><span class="sxs-lookup"><span data-stu-id="5060d-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="5060d-141">必須提供製造商名稱或至少一個當地語系化版本的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="5060d-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="5060d-142">必須提供模型名稱或至少一個當地語系化版本的模型名稱。</span><span class="sxs-lookup"><span data-stu-id="5060d-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="5060d-143">接著會使用 [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) 元素來產生包含這項資訊的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="5060d-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="5060d-144">如果有 [**PnPXDeviceCategory**](pnpxdevicecategory.md) 元素，則 [**至少一個裝載**](hosted.md) 的元素必須同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="5060d-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="5060d-145">同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 **thisModelMetadata** 元素內必須有 **PnPXDeviceCategory** 元素。</span><span class="sxs-lookup"><span data-stu-id="5060d-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="5060d-146">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5060d-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5060d-147">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="5060d-147">Minimum supported system</span></span><br/> | <span data-ttu-id="5060d-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5060d-148">Windows Vista</span></span> |
| <span data-ttu-id="5060d-149">可以是空的</span><span class="sxs-lookup"><span data-stu-id="5060d-149">Can be empty</span></span>                        | <span data-ttu-id="5060d-150">否</span><span class="sxs-lookup"><span data-stu-id="5060d-150">No</span></span>            |



 

 




