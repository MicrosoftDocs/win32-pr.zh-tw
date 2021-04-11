---
description: ViewSpaces 限定詞會定義來源實例所在之命名空間的名稱和位置。 您可以在本機或遠端電腦上指定任何命名空間的組合。
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: ViewSpaces 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195034"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="7dac3-104">ViewSpaces 辨識符號</span><span class="sxs-lookup"><span data-stu-id="7dac3-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="7dac3-105">**ViewSpaces 限定詞** 會定義來源實例所在之命名空間的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="7dac3-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="7dac3-106">您可以在本機或遠端電腦上指定任何命名空間的組合。</span><span class="sxs-lookup"><span data-stu-id="7dac3-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="7dac3-107">下列範例會列出本機電腦上的兩個命名空間。</span><span class="sxs-lookup"><span data-stu-id="7dac3-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="7dac3-108">[視圖提供者](view-provider.md)會依列出查詢和命名空間的順序，將 [ViewSources 限定詞](viewsources-qualifier.md)中的來源查詢與 **ViewSpaces** 辨識符號中列出的命名空間相符。</span><span class="sxs-lookup"><span data-stu-id="7dac3-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="7dac3-109">一般來說， **ViewSpaces** 限定詞中所列的命名空間數目和 **ViewSources** 辨識符號中列出的查詢之間有一對一關聯性。</span><span class="sxs-lookup"><span data-stu-id="7dac3-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="7dac3-110">在某些情況下，您可能會想要針對兩個或多個命名空間來執行 ViewSources 限定詞中所列的查詢。</span><span class="sxs-lookup"><span data-stu-id="7dac3-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="7dac3-111">您可以使用雙冒號 "：：" 來分隔多個命名空間，此命名空間會由 **ViewSources** 陣列中的其中一個查詢來評估。</span><span class="sxs-lookup"><span data-stu-id="7dac3-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="7dac3-112">在下列範例中， [**ViewSources**](viewsources-qualifier.md) 陣列中的第一個查詢會針對第一對引號中的命名空間執行，第二個查詢則針對第二對引號中的三個命名空間，而第三個查詢則是針對第三對引號中的兩個命名空間進行。</span><span class="sxs-lookup"><span data-stu-id="7dac3-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="7dac3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dac3-113">Requirements</span></span>



| <span data-ttu-id="7dac3-114">需求</span><span class="sxs-lookup"><span data-stu-id="7dac3-114">Requirement</span></span> | <span data-ttu-id="7dac3-115">值</span><span class="sxs-lookup"><span data-stu-id="7dac3-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7dac3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dac3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7dac3-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dac3-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7dac3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dac3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7dac3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dac3-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7dac3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dac3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dac3-121">**視圖提供者專用的限定詞**</span><span class="sxs-lookup"><span data-stu-id="7dac3-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




