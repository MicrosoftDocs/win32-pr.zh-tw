---
title: 使用 ADSI 修改屬性
description: 為了修改屬性值，ADSI 會提供 IADs 和 IADs PutEx 方法。 這些方法會修改用戶端快取上的資料。 必須呼叫 IADs SetInfo 方法，才能認可目錄的變更。
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 修改屬性
- 屬性 ADSI、修改
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382857"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="89783-107">使用 ADSI 修改屬性</span><span class="sxs-lookup"><span data-stu-id="89783-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="89783-108">為了修改屬性值，ADSI 會提供 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put) 和 [**IADs PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法。</span><span class="sxs-lookup"><span data-stu-id="89783-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="89783-109">這些方法會修改用戶端快取上的資料。</span><span class="sxs-lookup"><span data-stu-id="89783-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="89783-110">必須呼叫 [**IADs SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法，才能認可目錄的變更。</span><span class="sxs-lookup"><span data-stu-id="89783-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="89783-111">在對 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)的單一呼叫中認可多個屬性變更時，如果無法修改任何單一屬性，則不會修改任何屬性。</span><span class="sxs-lookup"><span data-stu-id="89783-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="89783-112">例如，如果您修改 [**sn**](/windows/desktop/ADSchema/a-sn) 和 [**givenName**](/windows/desktop/ADSchema/a-givenname) 屬性，並清除使用者物件的 [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) 屬性，但沒有任何後續的 **SetInfo** 方法呼叫，則會在您呼叫 **SetInfo** 時輸入變更。</span><span class="sxs-lookup"><span data-stu-id="89783-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="89783-113">如果不允許有一或多項修改，因而無法執行，則在呼叫 **SetInfo** 期間不會輸入對屬性進行的任何集體修改。</span><span class="sxs-lookup"><span data-stu-id="89783-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="89783-114">[**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put)方法會接受屬性名稱和 variant 參數。</span><span class="sxs-lookup"><span data-stu-id="89783-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="89783-115">您可以使用這個方法來設定包含單一和多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="89783-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="89783-116">[**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)方法可讓您控制多重值屬性上的作業。</span><span class="sxs-lookup"><span data-stu-id="89783-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="89783-117">您可以附加、刪除、更新和清除現有的值。</span><span class="sxs-lookup"><span data-stu-id="89783-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="89783-118">**IADs. PutEx** 方法一律需要屬性值的 variant 陣列。</span><span class="sxs-lookup"><span data-stu-id="89783-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="89783-119">不過，您也可以使用這個方法來設定具有單一值的屬性。</span><span class="sxs-lookup"><span data-stu-id="89783-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="89783-120">[**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)方法會使用 [**ADS \_ 屬性 \_ 運算 \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)列舉列舉所指定的作業。</span><span class="sxs-lookup"><span data-stu-id="89783-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 