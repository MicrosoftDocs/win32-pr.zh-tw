---
title: 預設類別和關聯
description: 針對特定類別，單一類別可以關聯為預設類別。
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371862"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="048d6-103">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="048d6-103">Default Classes and Associations</span></span>

<span data-ttu-id="048d6-104">針對特定類別，單一類別可以關聯為預設類別。</span><span class="sxs-lookup"><span data-stu-id="048d6-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="048d6-105">每當需要物件的特定類別時，就會選取預設的類別。</span><span class="sxs-lookup"><span data-stu-id="048d6-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="048d6-106">雖然這對所有元件類別都沒有説明，但在不需要使用者介入的情況下，當特定類別必須從可能的類別清單中載入時，建立預設類別會很有説明。</span><span class="sxs-lookup"><span data-stu-id="048d6-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="048d6-107">系統管理員可以藉由操作登錄來定義可使用的類別。</span><span class="sxs-lookup"><span data-stu-id="048d6-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="048d6-108">若要建立預設類別與類別之間的關聯，請引入 CLSID 索引鍵，其 CLSID 與選擇作為預設的元件類別的 CATID 相同。</span><span class="sxs-lookup"><span data-stu-id="048d6-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="048d6-109">然後使用類別的預設類別 CLSID 的值，將 TreatAs 索引鍵新增至此索引鍵。</span><span class="sxs-lookup"><span data-stu-id="048d6-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="048d6-110">若要使用元件類別的預設類別，請使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**COGETCLASSOBJECT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)，指定 CLSID 參數的 CATID。</span><span class="sxs-lookup"><span data-stu-id="048d6-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="048d6-111">這會自動重新導向至建立為此分類預設值的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="048d6-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="048d6-112">登錄專案如下所示：</span><span class="sxs-lookup"><span data-stu-id="048d6-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="048d6-113">在安裝期間，元件可以檢查其類別目錄的任何預設類別機碼是否存在，並為使用者提供覆寫目前設定的選項。</span><span class="sxs-lookup"><span data-stu-id="048d6-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="048d6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="048d6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="048d6-115">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="048d6-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="048d6-116">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="048d6-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="048d6-117">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="048d6-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="048d6-118">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="048d6-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="048d6-119">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="048d6-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




