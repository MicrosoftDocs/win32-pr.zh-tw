---
title: 依容器功能分類
description: 元件通常需要容器中的特定功能，且不會使用不提供支援的容器。
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022016"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="e2ba2-103">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="e2ba2-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="e2ba2-104">元件通常需要容器中的特定功能，且不會使用不提供支援的容器。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="e2ba2-105">使用者介面應該篩選出需要容器不支援之功能的元件。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="e2ba2-106">為了達成此目的，元件可以依必要的容器功能分類。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="e2ba2-107">需要容器中的功能，但無法在不支援該功能的容器中運作的元件範例是簡單的框架 OLE 控制項。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="e2ba2-108">依容器功能分類可透過元件的 CLSID 機碼中的額外登錄機碼來完成：</span><span class="sxs-lookup"><span data-stu-id="e2ba2-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="e2ba2-109">如這個範例所示，元件可以屬於表示支援之功能的元件類別，以及表示所需功能的元件類別。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="e2ba2-110">在下列範例中，按鈕控制項是不支援其他功能的一般 OLE 控制項。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="e2ba2-111">它可在任何 OLE 控制項容器中運作。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="e2ba2-112">比較上述範例與下一個範例，如果容器支援，MyDBControl 可以使用 Visual Basic 資料系結。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="e2ba2-113">不過，已定義它，使其可在不支援 Visual Basic 資料系結的容器中運作 (可能) 不同的資料庫 API：</span><span class="sxs-lookup"><span data-stu-id="e2ba2-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="e2ba2-114">群組方塊控制項是一個簡單的框架控制項。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="e2ba2-115">它會依賴執行 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 介面的容器，而且只能在這類容器中正確運作：</span><span class="sxs-lookup"><span data-stu-id="e2ba2-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="e2ba2-116">支援 Visual Basic 資料繫結控制項，但不支援簡單框架控制項的容器，會指定 \_ \_ insert 控制項使用者介面的 catid 控制項和 catid VBDatabound。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="e2ba2-117">顯示給使用者的控制項清單會包含 CLSID \_ 按鈕和 clsid \_ MyDBControl。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="e2ba2-118">\_不會顯示 CLSID 的分組。</span><span class="sxs-lookup"><span data-stu-id="e2ba2-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2ba2-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2ba2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2ba2-120">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="e2ba2-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="e2ba2-121">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="e2ba2-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="e2ba2-122">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="e2ba2-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="e2ba2-123">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="e2ba2-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="e2ba2-124">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="e2ba2-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




