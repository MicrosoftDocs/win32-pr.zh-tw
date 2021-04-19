---
title: 依元件功能分類
description: 元件類別可以用來顯示所有已安裝元件的子集。
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967609"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="a0b65-103">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="a0b65-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="a0b65-104">元件類別可以用來顯示所有已安裝元件的子集。</span><span class="sxs-lookup"><span data-stu-id="a0b65-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="a0b65-105">每個元件類別都是由 GUID 所識別，稱為類別目錄識別碼 (CATID) 。</span><span class="sxs-lookup"><span data-stu-id="a0b65-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="a0b65-106">每個 CATID 都有一份清單，其中列出與地區設定相關的已標記、人們看得懂的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0b65-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="a0b65-107">Catid 清單和人們可讀取的名稱會儲存在登錄的已知位置中。</span><span class="sxs-lookup"><span data-stu-id="a0b65-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="a0b65-108">例如，所有可執行 OLE 檔內嵌功能的元件都可以在元件類別中分類。</span><span class="sxs-lookup"><span data-stu-id="a0b65-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="a0b65-109">在過去，這些物件會由登錄中的「可插入」機碼來識別。</span><span class="sxs-lookup"><span data-stu-id="a0b65-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="a0b65-110">若要改為使用元件類別目錄，將會在登錄中新增下列資訊：</span><span class="sxs-lookup"><span data-stu-id="a0b65-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="a0b65-111">每個執行對應至元件類別之功能的類別，會在登錄的 CLSID 機碼中列出該類別的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0b65-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="a0b65-112">由於單一元件可以支援各種功能，因此元件可以屬於多個元件類別。</span><span class="sxs-lookup"><span data-stu-id="a0b65-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="a0b65-113">例如，特定的 OLE 控制項可能會支援參與 OLE 檔內嵌、Microsoft Visual Basic 資料系結和網際網路功能所需的所有功能。</span><span class="sxs-lookup"><span data-stu-id="a0b65-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="a0b65-114">這類控制項會將下列資訊儲存在登錄中的 CLSID 機碼中：</span><span class="sxs-lookup"><span data-stu-id="a0b65-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="a0b65-115">利用這項資訊，容器可以列舉系統上所安裝的控制項，並只顯示支援容器所需功能的控制項。</span><span class="sxs-lookup"><span data-stu-id="a0b65-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="a0b65-116">使用元件類別可讓您依元件的實功能來分類元件。</span><span class="sxs-lookup"><span data-stu-id="a0b65-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0b65-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0b65-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b65-118">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="a0b65-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="a0b65-119">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="a0b65-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="a0b65-120">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="a0b65-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="a0b65-121">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="a0b65-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="a0b65-122">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="a0b65-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




