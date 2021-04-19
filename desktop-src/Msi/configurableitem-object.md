---
description: ConfigurableItem 物件代表 ModuleConfiguration 資料表中的單一資料列。
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: 'ConfigurableItem 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990810"
---
# <a name="configurableitem-object"></a><span data-ttu-id="666cc-103">ConfigurableItem 物件</span><span class="sxs-lookup"><span data-stu-id="666cc-103">ConfigurableItem object</span></span>

<span data-ttu-id="666cc-104">**ConfigurableItem 物件** 代表 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的單一資料列。</span><span class="sxs-lookup"><span data-stu-id="666cc-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="666cc-105">這是模組中單一可設定的「屬性」。</span><span class="sxs-lookup"><span data-stu-id="666cc-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="666cc-106">介面是由唯讀屬性組成，ModuleConfiguration 資料表中的每個資料行各一個。</span><span class="sxs-lookup"><span data-stu-id="666cc-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="666cc-107">介面定義如下所示。</span><span class="sxs-lookup"><span data-stu-id="666cc-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="666cc-108">成員</span><span class="sxs-lookup"><span data-stu-id="666cc-108">Members</span></span>

<span data-ttu-id="666cc-109">**ConfigurableItem** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="666cc-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="666cc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="666cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="666cc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="666cc-111">Properties</span></span>

<span data-ttu-id="666cc-112">**ConfigurableItem** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="666cc-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="666cc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="666cc-113">Property</span></span>                                                         | <span data-ttu-id="666cc-114">描述</span><span class="sxs-lookup"><span data-stu-id="666cc-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="666cc-115">**屬性**</span><span class="sxs-lookup"><span data-stu-id="666cc-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="666cc-116">在 ModuleConfiguration 資料表中，傳回這個物件記錄之屬性欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="666cc-117">**Context**</span><span class="sxs-lookup"><span data-stu-id="666cc-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="666cc-118">傳回 ModuleConfiguration 資料表中這個物件記錄的內容欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="666cc-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="666cc-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="666cc-120">傳回 ModuleConfiguration 資料表中這個物件記錄的 DefaultValue 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="666cc-121">**描述**</span><span class="sxs-lookup"><span data-stu-id="666cc-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="666cc-122">在 ModuleConfiguration 資料表中，傳回這個物件記錄之 Description 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="666cc-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="666cc-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="666cc-124">傳回 ModuleConfiguration 資料表中這個物件記錄的 DisplayName 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="666cc-125">**格式**</span><span class="sxs-lookup"><span data-stu-id="666cc-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="666cc-126">傳回 ModuleConfiguration 資料表中這個物件記錄之格式欄位的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="666cc-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="666cc-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="666cc-128">傳回 ModuleConfiguration 資料表中這個物件記錄之 HelpKeyword 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="666cc-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="666cc-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="666cc-130">傳回 ModuleConfiguration 資料表中這個物件記錄之 HelpLocation 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="666cc-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="666cc-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="666cc-132">在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中，傳回這個物件記錄之 [名稱] 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="666cc-133">**類型**</span><span class="sxs-lookup"><span data-stu-id="666cc-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="666cc-134">在 ModuleConfiguration 資料表中，傳回這個物件之記錄的類型欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="666cc-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="666cc-135">C++</span><span class="sxs-lookup"><span data-stu-id="666cc-135">C++</span></span>

<span data-ttu-id="666cc-136">介面 **IMsmConfigurableItem： IDispatch**</span><span class="sxs-lookup"><span data-stu-id="666cc-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="666cc-137">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="666cc-137">Interface ID</span></span>



| <span data-ttu-id="666cc-138">常數</span><span class="sxs-lookup"><span data-stu-id="666cc-138">Constant</span></span>                      | <span data-ttu-id="666cc-139">值</span><span class="sxs-lookup"><span data-stu-id="666cc-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="666cc-140">**IID \_ IMsmConfigurableItem**</span><span class="sxs-lookup"><span data-stu-id="666cc-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="666cc-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="666cc-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="666cc-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="666cc-142">Requirements</span></span>



| <span data-ttu-id="666cc-143">需求</span><span class="sxs-lookup"><span data-stu-id="666cc-143">Requirement</span></span> | <span data-ttu-id="666cc-144">值</span><span class="sxs-lookup"><span data-stu-id="666cc-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="666cc-145">版本</span><span class="sxs-lookup"><span data-stu-id="666cc-145">Version</span></span><br/> | <span data-ttu-id="666cc-146">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="666cc-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="666cc-147">標頭</span><span class="sxs-lookup"><span data-stu-id="666cc-147">Header</span></span><br/>  | <dl> <span data-ttu-id="666cc-148"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="666cc-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="666cc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="666cc-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="666cc-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="666cc-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




