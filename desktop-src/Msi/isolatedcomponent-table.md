---
description: IsolatedComponent 資料表的每一筆記錄都會將 [元件應用程式] 資料 (行中指定的元件 \_ 與 [元件共用] 資料行中指定的元件) 產生關聯， \_ (通常是共用的 DLL) 。
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: IsolatedComponent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970435"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="4a9fb-103">IsolatedComponent 資料表</span><span class="sxs-lookup"><span data-stu-id="4a9fb-103">IsolatedComponent Table</span></span>

<span data-ttu-id="4a9fb-104">IsolatedComponent 資料表的每一筆記錄都會將 [元件應用程式] 資料 (行中指定的元件 \_ 與 [元件共用] 資料行中指定的元件) 產生關聯， \_ (通常是共用的 DLL) 。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="4a9fb-105">[IsolateComponents 動作](isolatecomponents-action.md)會將共用的元件複本安裝 \_ 到私人位置，以供元件 \_ 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="4a9fb-106">這會將元件 \_ 應用程式與其他共用的元件複本隔離，而該元件 \_ 可能會安裝到電腦上的共用位置。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="4a9fb-107">請參閱 [獨立元件](isolated-components.md)。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="4a9fb-108">若要連結一個 \_ 與多個元件 \_ 應用程式共用的元件，請在 IsolatedComponents 資料表中包含每個配對的個別記錄。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="4a9fb-109">安裝程式會將共用的元件檔案複製 \_ 到所安裝之每個元件應用程式的目錄中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="4a9fb-110">IsolatedComponent 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="4a9fb-111">Column</span><span class="sxs-lookup"><span data-stu-id="4a9fb-111">Column</span></span>                 | <span data-ttu-id="4a9fb-112">類型</span><span class="sxs-lookup"><span data-stu-id="4a9fb-112">Type</span></span>                         | <span data-ttu-id="4a9fb-113">答案</span><span class="sxs-lookup"><span data-stu-id="4a9fb-113">Key</span></span> | <span data-ttu-id="4a9fb-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="4a9fb-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="4a9fb-115">元件 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="4a9fb-115">Component\_Shared</span></span>      | [<span data-ttu-id="4a9fb-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="4a9fb-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="4a9fb-117">Y</span><span class="sxs-lookup"><span data-stu-id="4a9fb-117">Y</span></span>   | <span data-ttu-id="4a9fb-118">N</span><span class="sxs-lookup"><span data-stu-id="4a9fb-118">N</span></span>        |
| <span data-ttu-id="4a9fb-119">元件 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="4a9fb-119">Component\_Application</span></span> | [<span data-ttu-id="4a9fb-120">識別碼</span><span class="sxs-lookup"><span data-stu-id="4a9fb-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="4a9fb-121">Y</span><span class="sxs-lookup"><span data-stu-id="4a9fb-121">Y</span></span>   | <span data-ttu-id="4a9fb-122">N</span><span class="sxs-lookup"><span data-stu-id="4a9fb-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4a9fb-123">資料行</span><span class="sxs-lookup"><span data-stu-id="4a9fb-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4a9fb-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>元件 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="4a9fb-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="4a9fb-125">[元件資料表](component-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="4a9fb-126">包含共用檔案的元件，通常是 DLL。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="4a9fb-127">DLL 應該是此元件的金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="4a9fb-128">這必須與 [元件應用程式] 資料行中所列的元件不同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="4a9fb-129">共用元件會控制元件之所有隔離複本的註冊，而且必須在元件資料表的 [屬性] 資料行中設定 **msidbComponentAttributesSharedDllRefCount** 旗標。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="4a9fb-130">這樣可確保安裝程式可以管理共用元件的存留期。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="4a9fb-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>元件 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="4a9fb-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="4a9fb-132">[元件資料表](component-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="4a9fb-133">元件，包含載入共用檔案的 .exe。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="4a9fb-134">.Exe 應該是此元件的金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="4a9fb-135">這必須與元件共用資料行中所列的元件不同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a9fb-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="4a9fb-136">驗證</span><span class="sxs-lookup"><span data-stu-id="4a9fb-136">Validation</span></span>

<dl>

[<span data-ttu-id="4a9fb-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="4a9fb-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4a9fb-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="4a9fb-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4a9fb-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="4a9fb-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="4a9fb-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="4a9fb-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="4a9fb-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="4a9fb-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="4a9fb-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="4a9fb-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



