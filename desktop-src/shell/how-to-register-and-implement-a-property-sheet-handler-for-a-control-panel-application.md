---
description: 許多主控台應用程式會顯示內容內容表，讓使用者能夠查看和修改各種裝置和系統設定。
title: 如何註冊和執行主控台應用程式的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849190"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7460e-103">如何註冊和執行主控台應用程式的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="7460e-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7460e-104">許多主控台應用程式會顯示內容內容表，讓使用者能夠查看和修改各種裝置和系統設定。</span><span class="sxs-lookup"><span data-stu-id="7460e-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="7460e-105">這兩個應用程式（滑鼠和顯示器）可以讓屬性工作表處理常式以自訂頁面取代一或多個頁面。</span><span class="sxs-lookup"><span data-stu-id="7460e-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="7460e-106">下列螢幕擷取畫面顯示 [ **滑鼠屬性** ] 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="7460e-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![滑鼠屬性屬性工作表](images/propsheethandler3.jpg)

<span data-ttu-id="7460e-108">主控台應用程式的屬性工作表處理常式類似于檔案類型，但有兩個主要例外：</span><span class="sxs-lookup"><span data-stu-id="7460e-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="7460e-109">它們是由主控台應用程式呼叫，而非 Shell。</span><span class="sxs-lookup"><span data-stu-id="7460e-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="7460e-110">以不同方式註冊它們。</span><span class="sxs-lookup"><span data-stu-id="7460e-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7460e-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7460e-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7460e-112">技術</span><span class="sxs-lookup"><span data-stu-id="7460e-112">Technologies</span></span>

-   <span data-ttu-id="7460e-113">殼層</span><span class="sxs-lookup"><span data-stu-id="7460e-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7460e-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="7460e-114">Prerequisites</span></span>

-   <span data-ttu-id="7460e-115">瞭解主控台</span><span class="sxs-lookup"><span data-stu-id="7460e-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="7460e-116">對快速鍵功能表的瞭解</span><span class="sxs-lookup"><span data-stu-id="7460e-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="7460e-117">指示</span><span class="sxs-lookup"><span data-stu-id="7460e-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7460e-118">步驟1：註冊主控台應用程式的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="7460e-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7460e-119">主控台的應用程式屬性工作表處理常式必須在主控台子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="7460e-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="7460e-120">此索引鍵可以位於兩個位置的其中一個，視處理常式是每個使用者或每部電腦而定。</span><span class="sxs-lookup"><span data-stu-id="7460e-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="7460e-121">針對每位使用者註冊，主控台子機碼是 **HKEY \_ CURRENT \_ user** \\ **主控台**。</span><span class="sxs-lookup"><span data-stu-id="7460e-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="7460e-122">如 Regstr 中所定義的宏 REGSTR \_ 路徑 \_ 控制台，可以在程式碼中用來取代 "主控台"。</span><span class="sxs-lookup"><span data-stu-id="7460e-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="7460e-123">針對每一電腦的註冊，此位置為：</span><span class="sxs-lookup"><span data-stu-id="7460e-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="7460e-124">您可以在程式碼中將此路徑稱為 HKEY \_ 本機 \_ 電腦 \\ REGSTR \_ 路徑 \_ CONTROLSFOLDER，並使用 \_ CONTROLSFOLDER 中定義的 REGSTR path \_ REGSTR 宏。</span><span class="sxs-lookup"><span data-stu-id="7460e-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="7460e-125">允許屬性工作表處理常式取代頁面的主控台應用程式，在主控台的子機碼底下有一個子機碼，名為的應用程式，例如滑鼠和顯示器。</span><span class="sxs-lookup"><span data-stu-id="7460e-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="7460e-126">應用程式的子機碼必須具有具有 **PropertySheetHandlers** 子機碼的 **shellex** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="7460e-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="7460e-127">若要註冊屬性工作表處理常式，請將其 GUID 新增至與主控台應用程式相關聯的 **PropertySheetHandlers** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="7460e-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="7460e-128">若要這樣做，請建立 **PropertySheetHandlers** 子機碼的子機碼，並為屬性工作表處理常式命名，並將其預設值設定為處理常式 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="7460e-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="7460e-129">下列範例會以每部電腦為單位，為滑鼠主控台的應用程式註冊屬性工作表處理常式。</span><span class="sxs-lookup"><span data-stu-id="7460e-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="7460e-130">若要以每位使用者為基礎來註冊，請將 **HKEY \_ 本機 \_ 電腦** \\ **REGSTR \_ 路徑 \_ CONTROLSFOLDER** 取代為 **HKEY \_ CURRENT \_ user** \\ **REGSTR \_ path \_ 控制台**。</span><span class="sxs-lookup"><span data-stu-id="7460e-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7460e-131">步驟2：為主控台應用程式執行屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="7460e-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7460e-132">執行主控台屬性工作表處理常式的程式，與 [如何針對檔案類型註冊和執行屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)中所討論的程式非常類似。</span><span class="sxs-lookup"><span data-stu-id="7460e-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="7460e-133">主要差異在於現在 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) 需要 nontoken 的執行，而不是 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)。</span><span class="sxs-lookup"><span data-stu-id="7460e-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="7460e-134">當主控台應用程式即將顯示其屬性工作表時，它會針對每個可取代的頁面呼叫屬性工作表處理常式的 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) 方法一次。</span><span class="sxs-lookup"><span data-stu-id="7460e-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="7460e-135">*UPageID* 參數會設定為頁面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7460e-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="7460e-136">可用頁面的識別碼定義于 Cplext 中。</span><span class="sxs-lookup"><span data-stu-id="7460e-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="7460e-137">下表列出目前可用的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7460e-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="7460e-138">頁面識別碼</span><span class="sxs-lookup"><span data-stu-id="7460e-138">Page ID</span></span>                      | <span data-ttu-id="7460e-139">Description</span><span class="sxs-lookup"><span data-stu-id="7460e-139">Description</span></span>         | <span data-ttu-id="7460e-140">主控台應用程式</span><span class="sxs-lookup"><span data-stu-id="7460e-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="7460e-141">CPLPAGE \_ 滑鼠 \_ 按鈕</span><span class="sxs-lookup"><span data-stu-id="7460e-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="7460e-142">按鈕頁面</span><span class="sxs-lookup"><span data-stu-id="7460e-142">The Buttons page</span></span>    | <span data-ttu-id="7460e-143">滑鼠</span><span class="sxs-lookup"><span data-stu-id="7460e-143">Mouse</span></span>                     |
| <span data-ttu-id="7460e-144">CPLPAGE \_ 滑鼠 \_ PTRMOTION</span><span class="sxs-lookup"><span data-stu-id="7460e-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="7460e-145">[動作] 頁面</span><span class="sxs-lookup"><span data-stu-id="7460e-145">The Motion page</span></span>     | <span data-ttu-id="7460e-146">滑鼠</span><span class="sxs-lookup"><span data-stu-id="7460e-146">Mouse</span></span>                     |
| <span data-ttu-id="7460e-147">CPLPAGE \_ 滑鼠 \_ 滾輪</span><span class="sxs-lookup"><span data-stu-id="7460e-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="7460e-148">滾輪頁面</span><span class="sxs-lookup"><span data-stu-id="7460e-148">The Wheel page</span></span>      | <span data-ttu-id="7460e-149">滑鼠</span><span class="sxs-lookup"><span data-stu-id="7460e-149">Mouse</span></span>                     |
| <span data-ttu-id="7460e-150">CPLPAGE \_ 鍵盤 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="7460e-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="7460e-151">[速度] 頁面</span><span class="sxs-lookup"><span data-stu-id="7460e-151">The Speed page</span></span>      | <span data-ttu-id="7460e-152">鍵盤</span><span class="sxs-lookup"><span data-stu-id="7460e-152">Keyboard</span></span>                  |
| <span data-ttu-id="7460e-153">CPLPAGE \_ 顯示 \_ 背景</span><span class="sxs-lookup"><span data-stu-id="7460e-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="7460e-154">背景頁面</span><span class="sxs-lookup"><span data-stu-id="7460e-154">The Background page</span></span> | <span data-ttu-id="7460e-155">顯示</span><span class="sxs-lookup"><span data-stu-id="7460e-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="7460e-156">備註</span><span class="sxs-lookup"><span data-stu-id="7460e-156">Remarks</span></span>

<span data-ttu-id="7460e-157">建立和取代頁面的程式與新增頁面的程式相同。</span><span class="sxs-lookup"><span data-stu-id="7460e-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="7460e-158">如需詳細資訊，請參閱 [如何註冊和執行檔案類型的屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)。</span><span class="sxs-lookup"><span data-stu-id="7460e-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



