---
description: 存取集合的主要目的之一是從集合中移除專案。 您可以呼叫內含方法，從集合中移除專案。 Swbemobjectset 搭配使用或 SWbemMethodSet 無法使用這個方法。
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: 從 WMI 集合移除單一專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980768"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="df549-105">從 WMI 集合移除單一專案</span><span class="sxs-lookup"><span data-stu-id="df549-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="df549-106">存取集合的主要目的之一是從集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="df549-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="df549-107">您可以呼叫 [**內含**](swbempropertyset-remove.md) 方法，從集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="df549-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="df549-108">[**Swbemobjectset 搭配使用**](swbemobjectset.md)或 [**SWbemMethodSet**](swbemmethodset.md)無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="df549-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="df549-109">[**內含**](swbempropertyset.md)、 [**SWbemQualifierSet**](swbemqualifierset.md)和 [**SWbemNamedValueSet**](swbemnamedvalueset.md)中的名稱會移除專案。</span><span class="sxs-lookup"><span data-stu-id="df549-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="df549-110">不過， [**SWbemRefresher**](swbemrefresher.md) 中的專案會由索引移除，並由代表權限名稱的常數從 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 中移除。</span><span class="sxs-lookup"><span data-stu-id="df549-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="df549-111">**若要從集合中移除專案**</span><span class="sxs-lookup"><span data-stu-id="df549-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="df549-112">下列程式碼範例示範如何使用 [**內含**](swbempropertyset-remove.md) 方法來移除專案。</span><span class="sxs-lookup"><span data-stu-id="df549-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="df549-113">下列範例會在根預設命名空間中建立名為 "NewClass" 的新類別 \\ ，並在其中新增三個屬性。</span><span class="sxs-lookup"><span data-stu-id="df549-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="df549-114">腳本接著會使用前一個範例中的程式碼，刪除第二個屬性。</span><span class="sxs-lookup"><span data-stu-id="df549-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="df549-115">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [存取集合](accessing-a-collection.md)，以及 [從集合中移除多個專案](removing-multiple-items-from-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="df549-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



