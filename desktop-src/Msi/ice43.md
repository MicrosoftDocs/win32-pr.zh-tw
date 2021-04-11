---
description: ICE43 會驗證未將功能視為其目標 (非公告快速鍵的快捷方式) 是在具有 HKCU 登錄專案作為其金鑰路徑的元件中。
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115753"
---
# <a name="ice43"></a><span data-ttu-id="f436a-103">ICE43</span><span class="sxs-lookup"><span data-stu-id="f436a-103">ICE43</span></span>

<span data-ttu-id="f436a-104">ICE43 會驗證未將功能視為其目標 (非公告快速鍵的快捷方式) 是在具有 HKCU 登錄專案作為其金鑰路徑的元件中。</span><span class="sxs-lookup"><span data-stu-id="f436a-104">ICE43 validates that shortcuts that do not reference a feature as their Target (non-advertised shortcuts) are in components having a HKCU registry entry as their key path.</span></span>

## <a name="result"></a><span data-ttu-id="f436a-105">結果</span><span class="sxs-lookup"><span data-stu-id="f436a-105">Result</span></span>

<span data-ttu-id="f436a-106">如果非公告的快捷方式位於沒有 HKCU 登錄專案的元件中，ICE43 會張貼錯誤訊息做為它的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="f436a-106">ICE43 posts an error message if a non-advertised shortcut is in a component that does not have a HKCU registry entry as its key path.</span></span>

## <a name="example"></a><span data-ttu-id="f436a-107">範例</span><span class="sxs-lookup"><span data-stu-id="f436a-107">Example</span></span>

<span data-ttu-id="f436a-108">ICE43 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="f436a-108">ICE43 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="f436a-109">ICE43 錯誤</span><span class="sxs-lookup"><span data-stu-id="f436a-109">ICE43 error</span></span>                                                                                                                             | <span data-ttu-id="f436a-110">Description</span><span class="sxs-lookup"><span data-stu-id="f436a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f436a-111">元件 Component1 具有非公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f436a-111">Component Component1 has non-advertised shortcuts.</span></span> <span data-ttu-id="f436a-112">它必須使用 HKCU 下的登錄機碼作為其 KeyPath，而不是檔案。</span><span class="sxs-lookup"><span data-stu-id="f436a-112">It must use a registry key under HKCU as its KeyPath, not a file.</span></span>                    | <span data-ttu-id="f436a-113">Component1 的 attributes 資料行是0，這表示元件會使用檔案作為其 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="f436a-113">The attributes column of Component1 is 0, meaning that the component uses a file as its KeyPath.</span></span> <span data-ttu-id="f436a-114">如此一來，就只會針對電腦上的第一個使用者安裝此元件中的非公告快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f436a-114">This causes non-advertised shortcuts in this component to be installed for the first user on the computer ONLY.</span></span> <span data-ttu-id="f436a-115">稍後安裝元件的使用者看不到快捷方式，因為該元件在電腦上會顯示為已存在的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="f436a-115">Users who install the component later do not see the shortcuts because the component appear to the installer as already existing on the computer.</span></span> <span data-ttu-id="f436a-116">若要修正這個錯誤，請設定屬性的 RegistryKeyPath 位以將元件切換至登錄專案，然後將 KeyPath 值變更為登錄資料表中的有效專案。</span><span class="sxs-lookup"><span data-stu-id="f436a-116">To fix this error, set the RegistryKeyPath bit of the attributes to switch the Component to a Registry entry, then change the KeyPath value to a valid entry in the Registry table.</span></span><br/> |
| <span data-ttu-id="f436a-117">元件 Component2 具有非公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f436a-117">Component Component2 has non-advertised shortcuts.</span></span> <span data-ttu-id="f436a-118">它必須使用 HKCU 下的登錄機碼作為其 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="f436a-118">It must use a registry key under HKCU as its KeyPath.</span></span> <span data-ttu-id="f436a-119">KeyPath 目前為 null。</span><span class="sxs-lookup"><span data-stu-id="f436a-119">The KeyPath is currently null.</span></span> | <span data-ttu-id="f436a-120">[屬性] 資料行設定為使用登錄，但 KeyPath 為 null。</span><span class="sxs-lookup"><span data-stu-id="f436a-120">The Attributes column is set to use the registry, but the KeyPath is null.</span></span> <span data-ttu-id="f436a-121">KeyPath 必須參考登錄表中的專案。</span><span class="sxs-lookup"><span data-stu-id="f436a-121">The KeyPath must refer to an entry in the Registry Table.</span></span> <span data-ttu-id="f436a-122">若要修正這個錯誤，請將 KeyPath 值變更為登錄表中的有效專案。</span><span class="sxs-lookup"><span data-stu-id="f436a-122">To fix this error, change the KeyPath value to a valid entry in the Registry table.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f436a-123">元件 Component3 具有非公告的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f436a-123">Component Component3 has non-advertised shortcuts.</span></span> <span data-ttu-id="f436a-124">其 KeyPath 登錄機碼必須落在 HKCU 下。</span><span class="sxs-lookup"><span data-stu-id="f436a-124">Its KeyPath registry key must fall under HKCU.</span></span>                                       | <span data-ttu-id="f436a-125">[屬性] 資料行設定為使用登錄，但參考的登錄專案不在 HKCU 下。</span><span class="sxs-lookup"><span data-stu-id="f436a-125">The Attributes column is set to use the registry, but the referenced registry entry is not under HKCU.</span></span> <span data-ttu-id="f436a-126">若要修正這個錯誤，請切換到不同的登錄專案作為此元件的 KeyPath，或將登錄專案的根值變更為-1 或1。</span><span class="sxs-lookup"><span data-stu-id="f436a-126">To fix this error, either switch to a different registry entry as the KeyPath for this component, or change the Root value of the Registry entry to either -1 or 1.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f436a-127">元件 Component4 的 KeyPath 登錄專案不存在。</span><span class="sxs-lookup"><span data-stu-id="f436a-127">The KeyPath registry entry for component Component4 does not exist.</span></span>                                                                     | <span data-ttu-id="f436a-128">元件的 KeyPath 資料行中所參考的登錄專案不在登錄資料表中。</span><span class="sxs-lookup"><span data-stu-id="f436a-128">The Registry entry referenced in the KeyPath column of the component is not in the Registry Table.</span></span> <span data-ttu-id="f436a-129">若要修正這個錯誤，請建立一個專案。</span><span class="sxs-lookup"><span data-stu-id="f436a-129">To fix this error, create an entry.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f436a-130">登錄專案 Reg5 設定為元件 Component5 的 KeyPath，但該登錄專案不屬於 Component5。</span><span class="sxs-lookup"><span data-stu-id="f436a-130">The Registry Entry Reg5 is set as the KeyPath for component Component5, but that registry entry does not belong to Component5.</span></span>          | <span data-ttu-id="f436a-131">在 HKCU 樹狀目錄下的元件的 KeyPath 資料行中，有一個登錄專案參考，但是登錄專案的 Component 資料 \_ 行並未回頭參考到列為 KeyPath 的相同元件。</span><span class="sxs-lookup"><span data-stu-id="f436a-131">There is a Registry entry referenced in the KeyPath column of the component that lies under the HKCU tree, but the registry entry's Component\_ column does not refer back to the same component that listed it as the KeyPath.</span></span> <span data-ttu-id="f436a-132">這表示，只有在安裝其他元件時，才會建立用來做為元件 KeyPath 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="f436a-132">This means that the registry entry used as the KeyPath of the component is only created if some other component was installed.</span></span> <span data-ttu-id="f436a-133">若要修正這個錯誤，請將 KeyPath 值變更為參考屬於元件的登錄專案，或是將登錄專案變更為屬於 KeyPath 的元件。</span><span class="sxs-lookup"><span data-stu-id="f436a-133">To fix this error, change the KeyPath value to refer to a registry entry that belongs to the component or change the registry entry to belong to the component using it as a KeyPath.</span></span><br/>   |



 

<span data-ttu-id="f436a-134">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f436a-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f436a-135">元件</span><span class="sxs-lookup"><span data-stu-id="f436a-135">Component</span></span>  | <span data-ttu-id="f436a-136">屬性</span><span class="sxs-lookup"><span data-stu-id="f436a-136">Attributes</span></span> | <span data-ttu-id="f436a-137">KeyPath</span><span class="sxs-lookup"><span data-stu-id="f436a-137">KeyPath</span></span> |
|------------|------------|---------|
| <span data-ttu-id="f436a-138">Component1</span><span class="sxs-lookup"><span data-stu-id="f436a-138">Component1</span></span> | <span data-ttu-id="f436a-139">0</span><span class="sxs-lookup"><span data-stu-id="f436a-139">0</span></span>          | <span data-ttu-id="f436a-140">File1</span><span class="sxs-lookup"><span data-stu-id="f436a-140">File1</span></span>   |
| <span data-ttu-id="f436a-141">Component2</span><span class="sxs-lookup"><span data-stu-id="f436a-141">Component2</span></span> | <span data-ttu-id="f436a-142">4</span><span class="sxs-lookup"><span data-stu-id="f436a-142">4</span></span>          |         |
| <span data-ttu-id="f436a-143">Component3</span><span class="sxs-lookup"><span data-stu-id="f436a-143">Component3</span></span> | <span data-ttu-id="f436a-144">4</span><span class="sxs-lookup"><span data-stu-id="f436a-144">4</span></span>          | <span data-ttu-id="f436a-145">Reg3</span><span class="sxs-lookup"><span data-stu-id="f436a-145">Reg3</span></span>    |
| <span data-ttu-id="f436a-146">Component4</span><span class="sxs-lookup"><span data-stu-id="f436a-146">Component4</span></span> | <span data-ttu-id="f436a-147">4</span><span class="sxs-lookup"><span data-stu-id="f436a-147">4</span></span>          | <span data-ttu-id="f436a-148">Reg4</span><span class="sxs-lookup"><span data-stu-id="f436a-148">Reg4</span></span>    |
| <span data-ttu-id="f436a-149">Component5</span><span class="sxs-lookup"><span data-stu-id="f436a-149">Component5</span></span> | <span data-ttu-id="f436a-150">4</span><span class="sxs-lookup"><span data-stu-id="f436a-150">4</span></span>          | <span data-ttu-id="f436a-151">Reg5</span><span class="sxs-lookup"><span data-stu-id="f436a-151">Reg5</span></span>    |



 

<span data-ttu-id="f436a-152">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f436a-152">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="f436a-153">登錄</span><span class="sxs-lookup"><span data-stu-id="f436a-153">Registry</span></span> | <span data-ttu-id="f436a-154">Root</span><span class="sxs-lookup"><span data-stu-id="f436a-154">Root</span></span> | <span data-ttu-id="f436a-155">值</span><span class="sxs-lookup"><span data-stu-id="f436a-155">Value</span></span> | <span data-ttu-id="f436a-156">元件\_</span><span class="sxs-lookup"><span data-stu-id="f436a-156">Component\_</span></span> |
|----------|------|-------|-------------|
| <span data-ttu-id="f436a-157">Reg3</span><span class="sxs-lookup"><span data-stu-id="f436a-157">Reg3</span></span>     | <span data-ttu-id="f436a-158">2</span><span class="sxs-lookup"><span data-stu-id="f436a-158">2</span></span>    |       | <span data-ttu-id="f436a-159">Component3</span><span class="sxs-lookup"><span data-stu-id="f436a-159">Component3</span></span>  |
| <span data-ttu-id="f436a-160">Reg5</span><span class="sxs-lookup"><span data-stu-id="f436a-160">Reg5</span></span>     | <span data-ttu-id="f436a-161">0</span><span class="sxs-lookup"><span data-stu-id="f436a-161">0</span></span>    |       | <span data-ttu-id="f436a-162">Component4</span><span class="sxs-lookup"><span data-stu-id="f436a-162">Component4</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="f436a-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="f436a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f436a-164">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f436a-164">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




