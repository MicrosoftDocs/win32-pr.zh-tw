---
description: 在評估屬性策略之後，您必須決定要在 Windows 檔案總管 UI 中顯示哪些屬性，以及在何處顯示。
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: 使用屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade6cba2807e87306aa9cacb3649499d9e5ffe1
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481913"
---
# <a name="using-property-lists"></a><span data-ttu-id="81525-103">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="81525-103">Using Property Lists</span></span>

<span data-ttu-id="81525-104">在評估屬性策略之後，您必須決定要在 Windows 檔案總管 UI 中顯示哪些屬性，以及在何處顯示。</span><span class="sxs-lookup"><span data-stu-id="81525-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="81525-105">有各種不同的位置會以唯讀方式顯示內容。</span><span class="sxs-lookup"><span data-stu-id="81525-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="81525-106">另一方面，屬性編輯只會在 [ **屬性** ] 對話方塊中啟用。</span><span class="sxs-lookup"><span data-stu-id="81525-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="81525-107">您可以透過 **預覽窗格** 中的 [**編輯屬性**] 連結或專案的快捷方式功能表來叫用該對話方塊。</span><span class="sxs-lookup"><span data-stu-id="81525-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="81525-108">屬性清單是以分號分隔的字串，其格式如下。</span><span class="sxs-lookup"><span data-stu-id="81525-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="81525-109">下表顯示目前唯一可用的旗標。</span><span class="sxs-lookup"><span data-stu-id="81525-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="81525-110">旗標</span><span class="sxs-lookup"><span data-stu-id="81525-110">Flag</span></span> | <span data-ttu-id="81525-111">描述</span><span class="sxs-lookup"><span data-stu-id="81525-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="81525-112">請勿在 [ **預覽] 窗格** 中顯示內容，如 **PreviewDetails** 登錄機碼值中所指示。</span><span class="sxs-lookup"><span data-stu-id="81525-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="81525-113">如果未設定該屬性的值，請參閱下表後面的範例。</span><span class="sxs-lookup"><span data-stu-id="81525-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="81525-114">定義屬性清單之後，您可以透過 **HKEY \_ 類別 \_ 根目錄** 下的標準 [Shell 檔案關聯](../shell/fa-file-types.md)系統，將該字串儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="81525-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="81525-115">下表摘要說明可在特定副檔名的登錄機碼底下指派之屬性清單的值。</span><span class="sxs-lookup"><span data-stu-id="81525-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81525-116">值</span><span class="sxs-lookup"><span data-stu-id="81525-116">Value</span></span></th>
<th><span data-ttu-id="81525-117">描述</span><span class="sxs-lookup"><span data-stu-id="81525-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81525-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="81525-118">FullDetails</span></span></td>
<td><span data-ttu-id="81525-119">屬性會顯示在 [內容<strong>] 對話方塊的</strong>[<strong>詳細資料</strong>] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="81525-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="81525-120">這是檔案類型支援的完整屬性清單。</span><span class="sxs-lookup"><span data-stu-id="81525-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81525-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="81525-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="81525-122">屬性會顯示在 <strong>預覽窗格</strong>中。</span><span class="sxs-lookup"><span data-stu-id="81525-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81525-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="81525-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="81525-124">屬性會顯示在 [ <strong>預覽] 窗格</strong> 的標題區域中，位於專案的縮圖旁邊。</span><span class="sxs-lookup"><span data-stu-id="81525-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="81525-125">專案的數目上限為3。</span><span class="sxs-lookup"><span data-stu-id="81525-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="81525-126">如果屬性清單包含的數目超過允許的數目上限，則會忽略其餘的專案。</span><span class="sxs-lookup"><span data-stu-id="81525-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81525-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="81525-127">TileInfo</span></span></td>
<td><span data-ttu-id="81525-128">當清單視圖在 <strong>圖</strong> 格視圖模式中時，就會顯示內容。</span><span class="sxs-lookup"><span data-stu-id="81525-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="81525-129">專案的數目上限為3。</span><span class="sxs-lookup"><span data-stu-id="81525-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="81525-130">如果屬性清單包含的數目超過允許的數目上限，則會忽略其餘的專案。</span><span class="sxs-lookup"><span data-stu-id="81525-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="81525-131">此值存在於 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="81525-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81525-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="81525-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="81525-133">當清單視圖處於 <strong>擴充的並排</strong> 顯示模式時，會顯示專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="81525-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81525-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="81525-134">InfoTip</span></span></td>
<td><span data-ttu-id="81525-135">當使用者將滑鼠停留在專案上時，屬性會顯示在提示中。</span><span class="sxs-lookup"><span data-stu-id="81525-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="81525-136">此值存在於 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="81525-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81525-137">QuickTip</span><span class="sxs-lookup"><span data-stu-id="81525-137">QuickTip</span></span></td>
<td><span data-ttu-id="81525-138">當您很難直接從專案中取得屬性時，例如當必須透過慢速網路連接來存取專案時，就會顯示內容。</span><span class="sxs-lookup"><span data-stu-id="81525-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="81525-139">建議您在此處指定的屬性（例如類型或大小）不需要開啟檔案資料流程來決定其值。</span><span class="sxs-lookup"><span data-stu-id="81525-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="81525-140">此值存在於 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="81525-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="81525-141">下列範例會使用 **RecipeKey** 的 ProgID 來定義 PreviewDetails 的配方檔案類型值。</span><span class="sxs-lookup"><span data-stu-id="81525-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="81525-142">如 [Shell 檔案關聯](../shell/fa-file-types.md) 主題所述，檔案關聯可以針對最常見的最常見形式來描述。</span><span class="sxs-lookup"><span data-stu-id="81525-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="81525-143">最特定的形式是單一副檔名，最常見的形式是套用至所有檔案和檔案資料夾的金鑰。</span><span class="sxs-lookup"><span data-stu-id="81525-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="81525-144">在這兩個極端之間，您也可以定義一個 [PROGID](../shell/fa-progids.md) 來將一組副檔名群組在一起 (例如，將 .jpg 和 jpeg 類型分組為 **jpegfile**) 。</span><span class="sxs-lookup"><span data-stu-id="81525-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="81525-145">當您定義屬性清單時，您應該針對 Progid 或在某些情況下，針對特定的副檔名來定義它們。</span><span class="sxs-lookup"><span data-stu-id="81525-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="81525-146">避免依賴廣泛的專案，例如 **AllFileSystemObjects** 金鑰。</span><span class="sxs-lookup"><span data-stu-id="81525-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81525-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="81525-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81525-148">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="81525-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="81525-149">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="81525-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="81525-150">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="81525-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="81525-151">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="81525-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="81525-152">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="81525-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
