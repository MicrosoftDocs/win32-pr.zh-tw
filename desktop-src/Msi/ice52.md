---
description: ICE52 會檢查 AppSearch 資料表中的私用屬性。 請參閱關於屬性。
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851175"
---
# <a name="ice52"></a><span data-ttu-id="4b992-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="4b992-104">ICE52</span></span>

<span data-ttu-id="4b992-105">ICE52 會檢查 [AppSearch 資料表](appsearch-table.md)中的私用屬性。</span><span class="sxs-lookup"><span data-stu-id="4b992-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="4b992-106">請參閱 [關於屬性](about-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="4b992-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="4b992-107">使用 Windows 2000 時，AppSearch 資料表的屬性資料行中設定的所有屬性都必須是公用屬性。</span><span class="sxs-lookup"><span data-stu-id="4b992-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="4b992-108">結果</span><span class="sxs-lookup"><span data-stu-id="4b992-108">Result</span></span>

<span data-ttu-id="4b992-109">如果 AppSearch 資料表中有私用屬性，ICE52 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="4b992-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="4b992-110">範例</span><span class="sxs-lookup"><span data-stu-id="4b992-110">Example</span></span>

<span data-ttu-id="4b992-111">ICE52 會針對所顯示的範例張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="4b992-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="4b992-112">AppSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="4b992-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="4b992-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4b992-113">Property</span></span>  | <span data-ttu-id="4b992-114">簽名</span><span class="sxs-lookup"><span data-stu-id="4b992-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="4b992-115">PROPERTY1</span><span class="sxs-lookup"><span data-stu-id="4b992-115">PROPERTY1</span></span> | <span data-ttu-id="4b992-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="4b992-116">Signature1</span></span> |
| <span data-ttu-id="4b992-117">Property2</span><span class="sxs-lookup"><span data-stu-id="4b992-117">Property2</span></span> | <span data-ttu-id="4b992-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="4b992-118">Signature2</span></span> |



 

<span data-ttu-id="4b992-119">若要修正自訂公用屬性的這個警告變更： PROPERTY2。</span><span class="sxs-lookup"><span data-stu-id="4b992-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b992-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b992-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b992-121">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="4b992-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



