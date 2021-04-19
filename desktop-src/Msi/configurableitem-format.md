---
description: ConfigurableItem 物件的 Format 屬性會從 ModuleConfiguration 資料表的 Format 資料行傳回值。
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: 'ConfigurableItem： Format 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000804"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="5ba59-103">ConfigurableItem 格式屬性</span><span class="sxs-lookup"><span data-stu-id="5ba59-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="5ba59-104">[**ConfigurableItem**](configurableitem-object.md)物件的 **format** 屬性會從 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 format 資料行傳回值。</span><span class="sxs-lookup"><span data-stu-id="5ba59-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="5ba59-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5ba59-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba59-106">語法</span><span class="sxs-lookup"><span data-stu-id="5ba59-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="5ba59-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5ba59-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5ba59-108">備註</span><span class="sxs-lookup"><span data-stu-id="5ba59-108">Remarks</span></span>

<span data-ttu-id="5ba59-109">這個屬性只能包含下列值。</span><span class="sxs-lookup"><span data-stu-id="5ba59-109">This property can only have the following values.</span></span>



| <span data-ttu-id="5ba59-110">常數</span><span class="sxs-lookup"><span data-stu-id="5ba59-110">Constant</span></span>                        | <span data-ttu-id="5ba59-111">值</span><span class="sxs-lookup"><span data-stu-id="5ba59-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="5ba59-112">**msmConfigurableItemText**</span><span class="sxs-lookup"><span data-stu-id="5ba59-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="5ba59-113">0</span><span class="sxs-lookup"><span data-stu-id="5ba59-113">0</span></span>     |
| <span data-ttu-id="5ba59-114">**msmConfigurableItemKey**</span><span class="sxs-lookup"><span data-stu-id="5ba59-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="5ba59-115">1</span><span class="sxs-lookup"><span data-stu-id="5ba59-115">1</span></span>     |
| <span data-ttu-id="5ba59-116">**msmConfigurableItemInteger**</span><span class="sxs-lookup"><span data-stu-id="5ba59-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="5ba59-117">2</span><span class="sxs-lookup"><span data-stu-id="5ba59-117">2</span></span>     |
| <span data-ttu-id="5ba59-118">**msmConfigurableItemBitfield**</span><span class="sxs-lookup"><span data-stu-id="5ba59-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="5ba59-119">3</span><span class="sxs-lookup"><span data-stu-id="5ba59-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="5ba59-120">C++</span><span class="sxs-lookup"><span data-stu-id="5ba59-120">C++</span></span>

<span data-ttu-id="5ba59-121">請參閱 [**取得 \_ 格式**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) 函數。</span><span class="sxs-lookup"><span data-stu-id="5ba59-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ba59-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ba59-122">Requirements</span></span>



| <span data-ttu-id="5ba59-123">需求</span><span class="sxs-lookup"><span data-stu-id="5ba59-123">Requirement</span></span> | <span data-ttu-id="5ba59-124">值</span><span class="sxs-lookup"><span data-stu-id="5ba59-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba59-125">版本</span><span class="sxs-lookup"><span data-stu-id="5ba59-125">Version</span></span><br/> | <span data-ttu-id="5ba59-126">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5ba59-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5ba59-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5ba59-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5ba59-128"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba59-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ba59-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5ba59-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ba59-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ba59-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




