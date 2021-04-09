---
description: ICE92 會確認沒有元件識別碼 GUID 的元件也不會指定為永久元件。
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849972"
---
# <a name="ice92"></a><span data-ttu-id="02c97-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="02c97-103">ICE92</span></span>

<span data-ttu-id="02c97-104">ICE92 會確認沒有元件識別碼 GUID 的元件也不會指定為永久元件。</span><span class="sxs-lookup"><span data-stu-id="02c97-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="02c97-105">這個 ICE 自訂動作會檢查 [元件資料表](component-table.md) 中是否有未在 [元件識別碼] 欄位中指定 [GUID](guid.md) 的元件，並確認 [屬性] 欄位中尚未設定 **msidbComponentAttributesPermanent** 旗標。</span><span class="sxs-lookup"><span data-stu-id="02c97-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="02c97-106">ICE92 也會確認沒有任何元件同時有 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。</span><span class="sxs-lookup"><span data-stu-id="02c97-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="02c97-107">如果元件的資料行是 null，安裝程式就不會註冊元件，而且安裝程式無法移除或修復元件。</span><span class="sxs-lookup"><span data-stu-id="02c97-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="02c97-108">結果</span><span class="sxs-lookup"><span data-stu-id="02c97-108">Result</span></span>

<span data-ttu-id="02c97-109">ICE92 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="02c97-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="02c97-110">ICE92 錯誤</span><span class="sxs-lookup"><span data-stu-id="02c97-110">ICE92 error</span></span>                                                          | <span data-ttu-id="02c97-111">Description</span><span class="sxs-lookup"><span data-stu-id="02c97-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c97-112">元件 ' \[ 1 \] ' 沒有任何元件，並標示為永久。</span><span class="sxs-lookup"><span data-stu-id="02c97-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="02c97-113">元件資料表中此元件的專案在 [元件] 資料行中具有 null，且在 [屬性] 資料行中具有 **msidbComponentAttributesPermanent** 。</span><span class="sxs-lookup"><span data-stu-id="02c97-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="02c97-114">ICE92 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="02c97-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="02c97-115">ICE92 警告</span><span class="sxs-lookup"><span data-stu-id="02c97-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="02c97-116">Description</span><span class="sxs-lookup"><span data-stu-id="02c97-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c97-117">元件 ' \[ 1 \] ' 標示為永久和卸載取代。</span><span class="sxs-lookup"><span data-stu-id="02c97-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="02c97-118">因為元件是永久性的，所以會忽略取代取代屬性。</span><span class="sxs-lookup"><span data-stu-id="02c97-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="02c97-119">[元件資料表](component-table.md)中此元件的專案同時指定了 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。</span><span class="sxs-lookup"><span data-stu-id="02c97-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="02c97-120">範例</span><span class="sxs-lookup"><span data-stu-id="02c97-120">Example</span></span>

<span data-ttu-id="02c97-121">ICE92 會報告此範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="02c97-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="02c97-122">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="02c97-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="02c97-123">元件</span><span class="sxs-lookup"><span data-stu-id="02c97-123">Component</span></span>  | <span data-ttu-id="02c97-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="02c97-124">ComponentId</span></span> | <span data-ttu-id="02c97-125">目錄\_</span><span class="sxs-lookup"><span data-stu-id="02c97-125">Directory\_</span></span> | <span data-ttu-id="02c97-126">屬性</span><span class="sxs-lookup"><span data-stu-id="02c97-126">Attributes</span></span> | <span data-ttu-id="02c97-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="02c97-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="02c97-128">Component1</span><span class="sxs-lookup"><span data-stu-id="02c97-128">Component1</span></span> |             | <span data-ttu-id="02c97-129">DirectoryA</span><span class="sxs-lookup"><span data-stu-id="02c97-129">DirectoryA</span></span>  | <span data-ttu-id="02c97-130">16</span><span class="sxs-lookup"><span data-stu-id="02c97-130">16</span></span>         | <span data-ttu-id="02c97-131">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="02c97-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="02c97-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="02c97-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02c97-133">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="02c97-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



