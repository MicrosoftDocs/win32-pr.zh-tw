---
description: 如何執行和註冊 drop handler。
title: 如何建立 Drop 處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192688"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="02805-103">如何建立 Drop 處理常式</span><span class="sxs-lookup"><span data-stu-id="02805-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="02805-104">依預設，檔案不會放置目標。</span><span class="sxs-lookup"><span data-stu-id="02805-104">By default, files are not drop targets.</span></span> <span data-ttu-id="02805-105">您可以藉由執行和註冊卸載 *處理常式*，讓 [檔案類型](fa-file-types.md)的成員成為卸載目標。</span><span class="sxs-lookup"><span data-stu-id="02805-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="02805-106">如果已針對檔案類型註冊卸載處理常式，每當在檔案類型的成員上拖曳物件時，就會呼叫該處理常式。</span><span class="sxs-lookup"><span data-stu-id="02805-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="02805-107">Shell 會藉由在處理常式的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面上呼叫適當的方法來管理作業。</span><span class="sxs-lookup"><span data-stu-id="02805-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="02805-108">[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="02805-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="02805-109">本檔著重于卸載處理常式特定的執行層面。</span><span class="sxs-lookup"><span data-stu-id="02805-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="02805-110">指示</span><span class="sxs-lookup"><span data-stu-id="02805-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="02805-111">步驟1：執行 Drop 處理常式</span><span class="sxs-lookup"><span data-stu-id="02805-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="02805-112">就像所有 Shell 擴充處理常式一樣，卸載處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="02805-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="02805-113">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)外，還會匯出兩個介面。</span><span class="sxs-lookup"><span data-stu-id="02805-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="02805-114">Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="02805-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="02805-115">它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="02805-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="02805-116">如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="02805-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="02805-117">當卸載處理常式初始化後，Shell 會在處理常式的 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面上呼叫適當的方法。</span><span class="sxs-lookup"><span data-stu-id="02805-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="02805-118">步驟2：註冊 Drop 處理常式</span><span class="sxs-lookup"><span data-stu-id="02805-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="02805-119">捨棄處理常式會在此檔案類型的子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="02805-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="02805-120">針對處理常式建立名為 **DropHandler** 的子機碼，並將子機碼的預設值設定為處理常式 CLSID GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="02805-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="02805-121">如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="02805-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="02805-122">下列範例說明可針對 myp 檔案類型啟用 drop handler 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="02805-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="02805-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="02805-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02805-124">建立 Shell 擴充功能處理常式</span><span class="sxs-lookup"><span data-stu-id="02805-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="02805-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="02805-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="02805-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="02805-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
