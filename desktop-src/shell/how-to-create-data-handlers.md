---
description: 使用自訂資料格式處理常式來擴充剪貼簿。
title: 如何建立資料處理程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991566"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="24c8a-103">如何建立資料處理程式</span><span class="sxs-lookup"><span data-stu-id="24c8a-103">How to Create Data Handlers</span></span>

<span data-ttu-id="24c8a-104">將檔案複製到剪貼簿或拖放時，Shell 會建立支援各種標準 [剪貼簿格式](dragdrop.md)的資料物件。</span><span class="sxs-lookup"><span data-stu-id="24c8a-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="24c8a-105">針對特定檔案類型的檔案，您可以藉由執行和註冊 *資料處理程式* 來擴充可用的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="24c8a-106">當傳送檔案類型的檔案時，如果使用其中一種自訂格式，Shell 會將對資料物件之 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面的呼叫委派給資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="24c8a-107">[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="24c8a-108">本檔著重于資料處理程式專屬的實作為這些層面。</span><span class="sxs-lookup"><span data-stu-id="24c8a-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="24c8a-109">執行資料處理程式</span><span class="sxs-lookup"><span data-stu-id="24c8a-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="24c8a-110">註冊資料處理程式</span><span class="sxs-lookup"><span data-stu-id="24c8a-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="24c8a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="24c8a-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="24c8a-112">指示</span><span class="sxs-lookup"><span data-stu-id="24c8a-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="24c8a-113">步驟1：執行資料處理程式</span><span class="sxs-lookup"><span data-stu-id="24c8a-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="24c8a-114">如同所有 Shell 延伸模組處理常式，資料處理程式都是同進程元件物件模型， (COM) 物件實作為 Dll。</span><span class="sxs-lookup"><span data-stu-id="24c8a-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="24c8a-115">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)外，還會匯出兩個介面。</span><span class="sxs-lookup"><span data-stu-id="24c8a-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="24c8a-116">Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="24c8a-117">它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="24c8a-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="24c8a-118">如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="24c8a-119">當資料處理程式初始化之後，如果使用其中一種自訂格式，Shell 會將來自資料物件的呼叫委派給處理常式的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="24c8a-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="24c8a-120">步驟2：註冊資料處理程式</span><span class="sxs-lookup"><span data-stu-id="24c8a-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="24c8a-121">資料處理程式會在檔案類型的 *ProgID* 子機碼下註冊，如下所示： **HKEY \_ 類別 \_ 根目錄** \\ *ProgID* \\ **shellex** \\ **DataHandler**</span><span class="sxs-lookup"><span data-stu-id="24c8a-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="24c8a-122">針對 **DataHandler** 下的處理常式建立名為的子機碼，並將該處理常式子機碼的預設值設定為處理常式 CLSID GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="24c8a-123">如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。</span><span class="sxs-lookup"><span data-stu-id="24c8a-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="24c8a-124">下列範例說明可針對 myp 檔案類型啟用資料處理程式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="24c8a-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="24c8a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="24c8a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c8a-126">建立 Shell 擴充功能處理常式</span><span class="sxs-lookup"><span data-stu-id="24c8a-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="24c8a-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="24c8a-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="24c8a-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="24c8a-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
