---
description: 許多取用者（例如動態指令碼事件取用者或命令列事件取用者）都具有具有範本限定詞的字串屬性。
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: 使用標準字串範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850751"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="ce10e-103">使用標準字串範本</span><span class="sxs-lookup"><span data-stu-id="ce10e-103">Using Standard String Templates</span></span>

<span data-ttu-id="ce10e-104">許多取用者（例如動態指令碼事件取用者或命令列事件取用者）都具有具有 **範本** 限定詞的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="ce10e-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="ce10e-105">這些屬性會使用標準字串範本，來建立由取用者實例和部分事件所設定的字串。</span><span class="sxs-lookup"><span data-stu-id="ce10e-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="ce10e-106">標準字串範本的結構類似于 Microsoft Windows 環境變數規格。</span><span class="sxs-lookup"><span data-stu-id="ce10e-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="ce10e-107">下列清單顯示範本語言的一些範例：</span><span class="sxs-lookup"><span data-stu-id="ce10e-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="ce10e-108">字串「此處的部分文字」一律會產生字串「這裡有一些文字」。</span><span class="sxs-lookup"><span data-stu-id="ce10e-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="ce10e-109">"% CPUUtilization%" 一律會產生所傳遞事件的 **CPUUtilization** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="ce10e-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="ce10e-110">如果屬性不是字串，則會轉換為字串;例如，"90" 或 "TRUE"。</span><span class="sxs-lookup"><span data-stu-id="ce10e-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="ce10e-111">「此處理器的 CPU 使用率目前為% CPUUtilization%」會將事件的 **CPUUtilization** 屬性值內嵌到字串中，產生像是「此處理器的 cpu 使用率目前為90」的內容。</span><span class="sxs-lookup"><span data-stu-id="ce10e-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="ce10e-112">"% TargetInstance. CPUUtilization%" 會抓取 **TargetInstance** 屬性之內嵌實例中的 **CPUUtilization** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="ce10e-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="ce10e-113">"%%" 會產生單一的% sign。</span><span class="sxs-lookup"><span data-stu-id="ce10e-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="ce10e-114">如果要抓取的屬性是陣列，則會以下列格式產生整個陣列：「 (1、5、10、1024) 」。</span><span class="sxs-lookup"><span data-stu-id="ce10e-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="ce10e-115">如果陣列中只有一個元素，則會省略括弧。</span><span class="sxs-lookup"><span data-stu-id="ce10e-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="ce10e-116">如果陣列中沒有任何元素，則會產生 " () "。</span><span class="sxs-lookup"><span data-stu-id="ce10e-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="ce10e-117">如果屬性為内嵌物件，則會產生物件的 MOF 表示， (類似 [**IWbemClassObject：： GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="ce10e-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="ce10e-118">如果要求的是物件內嵌陣列的屬性，則會將它視為具有陣列值的屬性。</span><span class="sxs-lookup"><span data-stu-id="ce10e-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="ce10e-119">例如：% MyEvents. TargetInstance. DriverLetter% 可能會產生 ' ( "C："、"D：" ) ' （如果 MyEvents 是內嵌實例修改事件的陣列）。</span><span class="sxs-lookup"><span data-stu-id="ce10e-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="ce10e-120">字串常值</span><span class="sxs-lookup"><span data-stu-id="ce10e-120">String Literals</span></span>

<span data-ttu-id="ce10e-121">成對引號內的所有內容都會被視為字串常值，而且不會被取代。</span><span class="sxs-lookup"><span data-stu-id="ce10e-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="ce10e-122">下列範例顯示編譯器針對「CPU 使用率為% CPUUtilization%」所看到的字串。</span><span class="sxs-lookup"><span data-stu-id="ce10e-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="ce10e-123">這個字串會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="ce10e-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="ce10e-124">另一方面，編譯器會看到「CPU 使用率為 \\ "% CPUUtilization%"」字串，如下所示 \\ 。</span><span class="sxs-lookup"><span data-stu-id="ce10e-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="ce10e-125">這個字串會產生下列輸出，不含變數替代。</span><span class="sxs-lookup"><span data-stu-id="ce10e-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="ce10e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce10e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce10e-127">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="ce10e-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



