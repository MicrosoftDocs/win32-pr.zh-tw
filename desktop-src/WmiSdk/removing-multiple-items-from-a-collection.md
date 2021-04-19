---
description: 如果您嘗試移除集合中的一個以上的專案，您可能會發現某些專案未移除。
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: 從 WMI 集合移除多個專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982725"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="7e786-103">從 WMI 集合移除多個專案</span><span class="sxs-lookup"><span data-stu-id="7e786-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="7e786-104">如果您嘗試移除集合中的一個以上的專案，您可能會發現某些專案未移除。</span><span class="sxs-lookup"><span data-stu-id="7e786-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="7e786-105">您無法在移除專案時逐一查看集合，因為當您從集合中移除專案時，集合指標會移至下一個元素。</span><span class="sxs-lookup"><span data-stu-id="7e786-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="7e786-106">例如，嘗試從集合中移除所有專案會導致移除其他所有專案。</span><span class="sxs-lookup"><span data-stu-id="7e786-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="7e786-107">當您使用 [**SWbemQualifierSet**](swbemqualifierset-remove.md) 移除專案時，可能會看到此問題。請移除或 [**內含移除**](swbempropertyset-remove.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7e786-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="7e786-108">若要避免這個問題，您可以逐一查看集合，並在陣列中放置要移除的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="7e786-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="7e786-109">然後，您可以在陣列中執行迴圈，並刪除陣列中命名的專案。</span><span class="sxs-lookup"><span data-stu-id="7e786-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="7e786-110">集合（例如 [**SWbemNamedValueSet**](swbemnamedvalueset.md)、 [**SWbemPrivilegeSet**](swbemprivilegeset.md)和 [**SWbemRefresher**](swbemrefresher.md)）也有一種方法，可刪除複習容器中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="7e786-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="7e786-111">下列腳本說明如何從集合中移除數個專案。</span><span class="sxs-lookup"><span data-stu-id="7e786-111">The following script illustrates how to remove several items from a collection.</span></span>


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



您無法移除具有繼承屬性之類別實例或衍生類別中的屬性和限定詞。 這類刪除嘗試會引發錯誤，而且不會移除屬性或辨識符號;相反地，WMI 會將屬性或辨識符號重設為預設值。 <span data-ttu-id="7e786-114">如果衍生類別具有繼承的屬性，WMI 會將繼承的屬性重設為父類別中屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="7e786-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="7e786-115">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [存取集合](accessing-a-collection.md)，以及 [從集合中移除單一專案](removing-a-single-item-from-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="7e786-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 



