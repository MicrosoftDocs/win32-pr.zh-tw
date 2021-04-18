---
title: ActiveX 控制項登錄資訊
description: ActiveX 控制項登錄資訊
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508148"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="0e052-103">ActiveX 控制項登錄資訊</span><span class="sxs-lookup"><span data-stu-id="0e052-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="0e052-104">有一些登錄專案和旗標會使用。</span><span class="sxs-lookup"><span data-stu-id="0e052-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="0e052-105">此外，控制項可以支援元件類別，以分類它們所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="0e052-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="0e052-106">與控制項相關的登錄機碼會在下列樹狀結構中標示為星號：</span><span class="sxs-lookup"><span data-stu-id="0e052-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="0e052-107">**DefaultIcon** 專案是用來識別將控制項最小化至圖示時所要顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="0e052-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="0e052-108">[**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)函式是用來從取得圖示。DLL 或。指定的 EXE 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e052-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="0e052-109">**ToolboxBitmap32** 專案會識別 \* 要用於工具列或工具箱按鈕臉部的 16 15 點陣圖的模組名稱和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e052-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="0e052-110">標準 Windows 圖示大小太大，無法用於此用途。</span><span class="sxs-lookup"><span data-stu-id="0e052-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="0e052-111">此專案特別支援控制項容器，這些容器具有設計模式，其中一個會選取控制項，並將其放在設計的表單上。</span><span class="sxs-lookup"><span data-stu-id="0e052-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="0e052-112">例如，在 Visual Basic 中，控制項的圖示會在設計模式期間顯示于 Visual Basic 工具箱中。</span><span class="sxs-lookup"><span data-stu-id="0e052-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="0e052-113">**控制項** 專案會將物件標示為控制項。</span><span class="sxs-lookup"><span data-stu-id="0e052-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="0e052-114">容器通常會使用此專案來填滿對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0e052-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="0e052-115">容器會使用這個子機碼來判斷是否要在顯示控制項的對話方塊中包含物件。</span><span class="sxs-lookup"><span data-stu-id="0e052-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="0e052-116">可 **插入** 的子索引鍵也可以與控制項搭配使用，這取決於物件是否只能做為就地内嵌物件，且沒有特殊的控制項功能。</span><span class="sxs-lookup"><span data-stu-id="0e052-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="0e052-117">標記為 [插入] 的 **物件會顯示** 在其容器的 [插入物件] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="0e052-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="0e052-118">可 **插入** 的專案通常表示控制項已經過非控制項容器的測試。</span><span class="sxs-lookup"><span data-stu-id="0e052-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="0e052-119">可 **插入** 和 **控制** 子機碼都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0e052-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="0e052-120">如果控制項不是設計來使用不了解控制項的舊容器，則可以省略可 **插入** 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="0e052-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="0e052-121">如果控制項的設計目的是要使用特定的容器，而不想要插入其他容器中，則控制項可以省略該 **控制項** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0e052-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="0e052-122">控制項應該有屬性動詞、OLEIVERB \_ 屬性，以及它們所支援的任何其他動詞。</span><span class="sxs-lookup"><span data-stu-id="0e052-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="0e052-123">Properties 動詞以及標準動詞 OLEIVERB \_ PRIMARY，會指示控制項顯示其屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="0e052-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="0e052-124">當控制項為使用中時，[屬性] 動詞會顯示為容器功能表上的 [屬性] 專案。</span><span class="sxs-lookup"><span data-stu-id="0e052-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="0e052-125">如此一來，控制項可以顯示自己的屬性頁，讓使用者有一些實用的功能，即使容器不會處理控制項。</span><span class="sxs-lookup"><span data-stu-id="0e052-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="0e052-126">控制項會定義 **MiscStatus** 索引鍵，以描述其本身至可能的容器。</span><span class="sxs-lookup"><span data-stu-id="0e052-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="0e052-127">Bits 會採用 [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)的值，而控制項會將數個值新增至此列舉。</span><span class="sxs-lookup"><span data-stu-id="0e052-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="0e052-128">如需詳細資訊，請參閱 **OLEMISC** 列舉值。</span><span class="sxs-lookup"><span data-stu-id="0e052-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="0e052-129">用戶端可以呼叫 [**IOleObject：： GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) 來取得這項資訊，而不需要先將控制項具現化。</span><span class="sxs-lookup"><span data-stu-id="0e052-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="0e052-130">最後， **version** 描述的控制項版本應符合與此控制項相關聯之類型程式庫的版本。</span><span class="sxs-lookup"><span data-stu-id="0e052-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="0e052-131">此外，在控制項的類型資訊中，屬性控制項會將 coclass 專案標記為描述控制項。</span><span class="sxs-lookup"><span data-stu-id="0e052-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 