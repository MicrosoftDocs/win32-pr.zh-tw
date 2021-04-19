---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型35。
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: 自訂動作類型35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001755"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="6c8d4-103">自訂動作類型35</span><span class="sxs-lookup"><span data-stu-id="6c8d4-103">Custom Action Type 35</span></span>

<span data-ttu-id="6c8d4-104">此自訂動作會從格式化的文字字串設定安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="6c8d4-105">如需詳細資訊，請參閱 [變更目錄的目標位置。](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="6c8d4-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="6c8d4-106">來源</span><span class="sxs-lookup"><span data-stu-id="6c8d4-106">Source</span></span>

<span data-ttu-id="6c8d4-107">[CustomAction 資料表](customaction-table.md)的來源欄位包含[目錄資料表](directory-table.md)的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="6c8d4-108">指定的目錄是使用 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)，以目標欄位中的格式化字串來設定。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="6c8d4-109">這會將目標路徑和相關聯的屬性設定為目標欄位中格式化文字字串的展開值。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="6c8d4-110">在 [維護安裝](maintenance-installation.md)期間，請勿嘗試變更目標目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="6c8d4-111">如果已針對任何使用者安裝使用該路徑的某些元件，請不要嘗試變更目標目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="6c8d4-112">類型值</span><span class="sxs-lookup"><span data-stu-id="6c8d4-112">Type Value</span></span>

<span data-ttu-id="6c8d4-113">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="6c8d4-114">常數</span><span class="sxs-lookup"><span data-stu-id="6c8d4-114">Constants</span></span>                                                              | <span data-ttu-id="6c8d4-115">十六進位</span><span class="sxs-lookup"><span data-stu-id="6c8d4-115">Hexadecimal</span></span> | <span data-ttu-id="6c8d4-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="6c8d4-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="6c8d4-117">**msidbCustomActionTypeTextData**  + **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="6c8d4-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="6c8d4-118">0x023</span><span class="sxs-lookup"><span data-stu-id="6c8d4-118">0x023</span></span>       | <span data-ttu-id="6c8d4-119">35</span><span class="sxs-lookup"><span data-stu-id="6c8d4-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="6c8d4-120">目標</span><span class="sxs-lookup"><span data-stu-id="6c8d4-120">Target</span></span>

<span data-ttu-id="6c8d4-121">[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="6c8d4-122">要取代的參數會以方括弧括住 \[ \] ，而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="6c8d4-123">請注意，目錄路徑一律以目錄分隔符號結尾。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="6c8d4-124">傳回處理選項</span><span class="sxs-lookup"><span data-stu-id="6c8d4-124">Return Processing Options</span></span>

<span data-ttu-id="6c8d4-125">自訂動作不會使用這些選項。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="6c8d4-126">執行排程選項</span><span class="sxs-lookup"><span data-stu-id="6c8d4-126">Execution Scheduling Options</span></span>

<span data-ttu-id="6c8d4-127">在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="6c8d4-128">這些選項控制多個自訂動作的執行。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="6c8d4-129">如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="6c8d4-130">In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="6c8d4-130">In-Script Execution Options</span></span>

<span data-ttu-id="6c8d4-131">自訂動作不會使用這些選項。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c8d4-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c8d4-132">Return Values</span></span>

<span data-ttu-id="6c8d4-133">請參閱 [自訂動作傳回值](custom-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8d4-134">備註</span><span class="sxs-lookup"><span data-stu-id="6c8d4-134">Remarks</span></span>

<span data-ttu-id="6c8d4-135">如果您在 UI 序列中，藉由在其中一個使用者介面順序資料表中撰寫自訂動作來設定 [私用屬性](private-properties.md) ，該屬性就不會在執行順序中設定。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="6c8d4-136">若要在執行順序中設定屬性，您也必須在執行順序資料表中放置自訂動作。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="6c8d4-137">或者，您可以將屬性設為 [公用屬性](public-properties.md) ，並將它包含在 [**SecureCustomProperties 屬性**](securecustomproperties.md)中。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c8d4-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c8d4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c8d4-139">自訂 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="6c8d4-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6c8d4-140">格式化的文本自訂動作</span><span class="sxs-lookup"><span data-stu-id="6c8d4-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



