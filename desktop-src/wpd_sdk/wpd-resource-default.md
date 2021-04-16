---
description: 指定物件後方的整個檔案。 它也是參考任何資源類型的方式，包括其他 Windows 可攜式裝置資源類型未涵蓋的資源類型，例如自訂物件類型。
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513921"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="94072-104">WPD \_ 資源 \_ 預設</span><span class="sxs-lookup"><span data-stu-id="94072-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="94072-105">指定物件後方的整個檔案。</span><span class="sxs-lookup"><span data-stu-id="94072-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="94072-106">它也是參考任何資源類型的方式，包括其他 Windows 可攜式裝置資源類型未涵蓋的資源類型，例如自訂物件類型。</span><span class="sxs-lookup"><span data-stu-id="94072-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="94072-107">將包含內嵌于指定資源內的任何資源。</span><span class="sxs-lookup"><span data-stu-id="94072-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="94072-108">例如，連絡人根資料夾的預設資源可能包含所有嵌套的連絡人。</span><span class="sxs-lookup"><span data-stu-id="94072-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="94072-109">但是，任何僅由中繼資料或參考所 *連結* 的子資源都不會包含在內。</span><span class="sxs-lookup"><span data-stu-id="94072-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="94072-110">其中一個範例就是播放清單，它可能只會透過中繼資料參考或檔案中的文字路徑參考連結到音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="94072-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="94072-111">此 **PROPERTYKEY** 唯一允許的 *pid* 值為零。</span><span class="sxs-lookup"><span data-stu-id="94072-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="94072-112">這種類型的資源必須支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="94072-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="94072-113">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="94072-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="94072-114">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="94072-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="94072-115">WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="94072-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="94072-116">必要。</span><span class="sxs-lookup"><span data-stu-id="94072-116">Required.</span></span>                                              |
| [<span data-ttu-id="94072-117">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="94072-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="94072-118">如果用戶端可以讀取此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="94072-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="94072-119">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="94072-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="94072-120">如果用戶端可以寫入此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="94072-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="94072-121">WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="94072-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="94072-122">如果用戶端可以刪除此資源，則為必要。</span><span class="sxs-lookup"><span data-stu-id="94072-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="94072-123">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="94072-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="94072-124">如果用戶端擁有資源的讀取權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="94072-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="94072-125">WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="94072-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="94072-126">如果用戶端具有資源的寫入權限，則為必要。</span><span class="sxs-lookup"><span data-stu-id="94072-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="94072-127">WPD \_ 資源 \_ 屬性 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="94072-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="94072-128">必要。</span><span class="sxs-lookup"><span data-stu-id="94072-128">Required.</span></span>                                              |
| [<span data-ttu-id="94072-129">WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="94072-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="94072-130">建議使用。</span><span class="sxs-lookup"><span data-stu-id="94072-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="94072-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94072-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94072-132">**資源的需求**</span><span class="sxs-lookup"><span data-stu-id="94072-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



