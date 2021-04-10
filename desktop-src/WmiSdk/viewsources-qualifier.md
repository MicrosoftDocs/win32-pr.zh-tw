---
description: 所有視圖類別都必須有一個稱為 ViewSources 的字串陣列限定詞。
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: ViewSources 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693815"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="79e18-103">ViewSources 辨識符號</span><span class="sxs-lookup"><span data-stu-id="79e18-103">ViewSources Qualifier</span></span>

<span data-ttu-id="79e18-104">所有視圖類別都必須有一個稱為 **ViewSources** 的字串陣列限定詞。</span><span class="sxs-lookup"><span data-stu-id="79e18-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="79e18-105">**ViewSources** 限定詞包含定義 view 類別中所使用之來源實例的來源查詢。</span><span class="sxs-lookup"><span data-stu-id="79e18-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="79e18-106">**ViewSources** 限定詞的值是字串陣列，其中包含 [*(WQL)*](gloss-w.md)查詢的 WMI 查詢語言。</span><span class="sxs-lookup"><span data-stu-id="79e18-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="79e18-107">您可以定義來源類別，並限制 view 類別所使用的來源實例與使用 [WQL](querying-with-wql.md)[WHERE 子句](where-clause.md) 進行查詢，以建立篩選的視圖。</span><span class="sxs-lookup"><span data-stu-id="79e18-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="79e18-108">[視圖提供者](view-provider.md)會依列出查詢和命名空間的順序，將 **ViewSources** 限定詞中的來源查詢與 [ViewSpaces 辨識符號](viewspaces-qualifier.md)中列出的命名空間相符。</span><span class="sxs-lookup"><span data-stu-id="79e18-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="79e18-109">來源查詢的數目必須符合 ViewSpaces 限定詞中列出的命名空間數目。</span><span class="sxs-lookup"><span data-stu-id="79e18-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="79e18-110">您列出來源查詢的順序會決定來源實例繪製所在的命名空間。</span><span class="sxs-lookup"><span data-stu-id="79e18-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="79e18-111">下列範例只會選取 **LocalDisk** 類別的實例，其中 **FileSystem** 屬性的值是 "NTFS" 和 **RemoteDisk** 類別的實例，其中的可 **空間** 屬性值大於 45 mb：</span><span class="sxs-lookup"><span data-stu-id="79e18-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="79e18-112">您可以針對聯結視圖類別定義的來源查詢數目，取決於這些查詢所傳回的實例數目，以及這些實例可以聯結的方式有好幾種。</span><span class="sxs-lookup"><span data-stu-id="79e18-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="79e18-113">View 類別的來源實例可能組合的數目會以指數方式成長，因此請盡可能將聯結視圖類別的來源查詢保持在最簡單的情況。</span><span class="sxs-lookup"><span data-stu-id="79e18-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79e18-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="79e18-114">Requirements</span></span>



| <span data-ttu-id="79e18-115">需求</span><span class="sxs-lookup"><span data-stu-id="79e18-115">Requirement</span></span> | <span data-ttu-id="79e18-116">值</span><span class="sxs-lookup"><span data-stu-id="79e18-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="79e18-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79e18-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79e18-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79e18-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="79e18-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79e18-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79e18-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79e18-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79e18-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79e18-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e18-122">**視圖提供者專用的限定詞**</span><span class="sxs-lookup"><span data-stu-id="79e18-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




