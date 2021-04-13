---
description: 使用逗號和分號可能是最複雜的檔案格式語法問題，而這種用法非常嚴格。 逗號可用來分隔陣列成員;分號會終止每個資料項目。
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: 使用逗號和分號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109881"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="92552-104">使用逗號和分號</span><span class="sxs-lookup"><span data-stu-id="92552-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="92552-105">使用逗號和分號可能是最複雜的檔案格式語法問題，而這種用法非常嚴格。</span><span class="sxs-lookup"><span data-stu-id="92552-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="92552-106">逗號可用來分隔陣列成員;分號會終止每個資料項目。</span><span class="sxs-lookup"><span data-stu-id="92552-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="92552-107">例如，如果範本是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="92552-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="92552-108">然後，此範本的實例看起來如下所示：</span><span class="sxs-lookup"><span data-stu-id="92552-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="92552-109">如果範本包含另一個範本，則會以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="92552-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="92552-110">然後，此範本的實例看起來如下所示：</span><span class="sxs-lookup"><span data-stu-id="92552-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="92552-111">請注意，代表容器內 mytemp 的第二行在行尾有兩個分號。</span><span class="sxs-lookup"><span data-stu-id="92552-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="92552-112">第一個分號表示資料項目的結尾，aTemp (在容器) 內，而第二個分號表示容器的結尾。</span><span class="sxs-lookup"><span data-stu-id="92552-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="92552-113">如果陣列是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="92552-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="92552-114">然後，它的實例看起來如下所示：</span><span class="sxs-lookup"><span data-stu-id="92552-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="92552-115">在陣列範例中，資料項目目不需要以分號分隔，因為它們是以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="92552-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="92552-116">結尾的分號會標示陣列的結尾。</span><span class="sxs-lookup"><span data-stu-id="92552-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="92552-117">請考慮包含範本所定義之資料項目陣列的範本。</span><span class="sxs-lookup"><span data-stu-id="92552-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="92552-118">這種情況的實例看起來會如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="92552-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="92552-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="92552-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92552-120">文字編碼方式</span><span class="sxs-lookup"><span data-stu-id="92552-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



