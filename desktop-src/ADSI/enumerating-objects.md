---
title: 列舉物件
description: 若要查看容器的子物件（例如組織單位） (OU) ，請列舉容器物件。
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- 列舉物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839204"
---
# <a name="enumerating-objects"></a><span data-ttu-id="cf852-104">列舉物件</span><span class="sxs-lookup"><span data-stu-id="cf852-104">Enumerating Objects</span></span>

<span data-ttu-id="cf852-105">若要查看容器的子物件（例如組織單位） (OU) ，請列舉容器物件。</span><span class="sxs-lookup"><span data-stu-id="cf852-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="cf852-106">為了與檔案系統相類似，子物件會對應至目錄中的檔案，而容器（父物件）會對應至目錄本身。</span><span class="sxs-lookup"><span data-stu-id="cf852-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="cf852-107">當您想要取得物件的父物件時，也可以使用列舉作業。</span><span class="sxs-lookup"><span data-stu-id="cf852-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="cf852-108">當您列舉物件時，實際上會系結至目錄中的物件，並在每個物件上傳回 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面。</span><span class="sxs-lookup"><span data-stu-id="cf852-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="cf852-109">下列程式碼範例顯示如何列舉容器的子系。</span><span class="sxs-lookup"><span data-stu-id="cf852-109">The following code example shows how to enumerate the children of a container.</span></span>


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



<span data-ttu-id="cf852-110">您可以篩選從列舉傳回的物件類型。</span><span class="sxs-lookup"><span data-stu-id="cf852-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="cf852-111">例如，若只要顯示使用者和群組，請在列舉之前使用下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="cf852-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="cf852-112">如果您有物件參考，則可以使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**父**](iads-property-methods.md) 屬性取得物件的父系。</span><span class="sxs-lookup"><span data-stu-id="cf852-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="cf852-113">下列程式碼範例顯示如何系結至父物件。</span><span class="sxs-lookup"><span data-stu-id="cf852-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="cf852-114">如需詳細資訊，請參閱 [列舉 ADSI 物件](enumerating-adsi-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cf852-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf852-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf852-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf852-116">搜尋物件</span><span class="sxs-lookup"><span data-stu-id="cf852-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




