---
title: 在顯示規範中註冊內容功能表 COM 物件
description: 本主題說明需要修改才能註冊內容功能表 COM 物件的登錄機碼。
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- 在顯示規範中註冊內容功能表 COM 物件
- 內容功能表 COM 物件廣告，註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023223"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a><span data-ttu-id="fa626-105">在顯示規範中註冊內容功能表 COM 物件</span><span class="sxs-lookup"><span data-stu-id="fa626-105">Registering the Context Menu COM Object in a Display Specifier</span></span>

<span data-ttu-id="fa626-106">當您使用 COM 建立 Active Directory Directory 服務的內容功能表延伸 DLL 時，必須向 Windows 登錄註冊擴充功能，並 Active Directory Domain Services，以通知 Active Directory 的系統管理 MMC 嵌入式管理單元和 Windows shell 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fa626-106">When you use COM to create a context menu extension DLL for an Active Directory directory service, the extension must be registered with the Windows registry and Active Directory Domain Services to notify the Active Directory administrative MMC snap-ins and the Windows shell of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="fa626-107">在 Windows 登錄中註冊</span><span class="sxs-lookup"><span data-stu-id="fa626-107">Registering in the Windows Registry</span></span>

<span data-ttu-id="fa626-108">和所有 COM 伺服器一樣，必須在登錄中註冊內容功能表延伸。</span><span class="sxs-lookup"><span data-stu-id="fa626-108">Like all COM servers, a context menu extension must be registered in the registry.</span></span> <span data-ttu-id="fa626-109">此擴充功能會在下列機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="fa626-109">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="fa626-110">*<clsid>* 這是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函數所產生之 CLSID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="fa626-110">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="fa626-111">在機 *<clsid>* 碼下，有一個 **InProcServer32** 機碼會將物件識別為32位的內部進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="fa626-111">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="fa626-112">在 **InProcServer32** 索引鍵下，DLL 的位置會指定為預設值，而執行緒模型則是在 **>threadingmodel** 值中指定。</span><span class="sxs-lookup"><span data-stu-id="fa626-112">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="fa626-113">所有內容功能表延伸都必須使用「單元」執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="fa626-113">All context menu extension must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="fa626-114">向 Active Directory Domain Services 註冊</span><span class="sxs-lookup"><span data-stu-id="fa626-114">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="fa626-115">操作功能表延伸模組註冊是特定于一個地區設定。</span><span class="sxs-lookup"><span data-stu-id="fa626-115">Context menu extension registration is specific to one locale.</span></span> <span data-ttu-id="fa626-116">如果內容功能表延伸模組套用至所有地區設定，則必須在 [顯示規範] 容器中所有地區設定子容器的物件類別 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 物件中註冊。</span><span class="sxs-lookup"><span data-stu-id="fa626-116">If the context menu extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="fa626-117">如果內容功能表延伸針對特定地區設定進行當地語系化，則必須在該地區設定的 subcontainer 中，將它註冊在 **displaySpecifier** 物件中。</span><span class="sxs-lookup"><span data-stu-id="fa626-117">If the context menu extension is localized for a certain locale, it must be registered in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="fa626-118">如需顯示規範容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。</span><span class="sxs-lookup"><span data-stu-id="fa626-118">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="fa626-119">有兩個顯示規範屬性可以在其中註冊內容功能表延伸模組專案。</span><span class="sxs-lookup"><span data-stu-id="fa626-119">There are two display specifier attributes that a context menu extension item can be registered under.</span></span> <span data-ttu-id="fa626-120">這些都是 [**adminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) 和 [**shellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="fa626-120">These are [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) and [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).</span></span>

<span data-ttu-id="fa626-121">[**AdminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu)屬性會識別要在 Active Directory 系統管理嵌入式管理單元中顯示的系統管理內容功能表。當使用者在其中一個 Active Directory 系統管理 MMC 嵌入式管理單元中顯示適當類別的物件內容功能表時，就會顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="fa626-121">The [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) attribute identifies administrative context menus to display in Active Directory administrative snap-ins. The context menu appears when the user displays the context menu for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="fa626-122">[**ShellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu)屬性會識別要在 Windows shell 中顯示的使用者內容功能表。</span><span class="sxs-lookup"><span data-stu-id="fa626-122">The [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) attribute identifies end-user context menus to display in the Windows shell.</span></span> <span data-ttu-id="fa626-123">當使用者在 Windows 檔案總管中，流覽適當類別的物件內容功能表時，就會顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="fa626-123">The context menu appears when the user views the context menu for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="fa626-124">從 Windows Server 2003 開始，Windows shell 不再顯示 Active Directory Domain Services 的物件。</span><span class="sxs-lookup"><span data-stu-id="fa626-124">Beginning with Windows Server 2003, the Windows shell no longer displays objects of Active Directory Domain Services.</span></span>

<span data-ttu-id="fa626-125">所有這些屬性都是多重值。</span><span class="sxs-lookup"><span data-stu-id="fa626-125">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="fa626-126">註冊內容功能表延伸模組時， [**adminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) 和 [**shellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) 屬性的值需要下列格式。</span><span class="sxs-lookup"><span data-stu-id="fa626-126">When registering a context menu extension, the values for the [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) and [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) attributes require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="fa626-127">「 &lt; 訂單編號」 &gt; 是一個不帶正負號的數位，代表內容功能表中的專案位置。</span><span class="sxs-lookup"><span data-stu-id="fa626-127">The "&lt;order number&gt;" is an unsigned number that represents the item position in the context menu.</span></span> <span data-ttu-id="fa626-128">顯示內容功能表時，會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="fa626-128">When a context menu is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="fa626-129">如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，則這些內容功能表延伸模組會以從 Active Directory 伺服器讀取的順序載入。</span><span class="sxs-lookup"><span data-stu-id="fa626-129">If more than one value has the same "&lt;order number&gt;", those context menu extensions are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="fa626-130">可能的話，請使用非現有的「 &lt; 訂單編號」 &gt; ，也就是屬性中其他值尚未使用的「訂單編號」。</span><span class="sxs-lookup"><span data-stu-id="fa626-130">If possible, use a non-existing "&lt;order number&gt;", that is, one that has not been used by other values in the property.</span></span> <span data-ttu-id="fa626-131">「訂單編號」序列中不允許有指定的開始位置和間距 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="fa626-131">There is no prescribed starting position and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="fa626-132">" &lt; Clsid &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 clsid 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="fa626-132">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="fa626-133">在 Windows shell 中，支援多重選取的內容功能表項目。</span><span class="sxs-lookup"><span data-stu-id="fa626-133">In the Windows shell, multiple-selection context menu items are supported.</span></span> <span data-ttu-id="fa626-134">在此情況下，會針對每個選取的物件叫用內容功能表延伸。</span><span class="sxs-lookup"><span data-stu-id="fa626-134">In this case, the context menu extension is invoked for each selected object.</span></span> <span data-ttu-id="fa626-135">在 Active Directory 系統管理嵌入式管理單元中，也支援多重選取的內容功能表擴充功能專案。</span><span class="sxs-lookup"><span data-stu-id="fa626-135">In Active Directory administrative snap-ins, multiple-selection context menu extension items are also supported.</span></span> <span data-ttu-id="fa626-136">在此情況下， [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構將會包含所選取的每個目錄物件的 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。</span><span class="sxs-lookup"><span data-stu-id="fa626-136">In this case, the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure will contain a [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure for each directory object selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa626-137">針對 Windows shell，會在使用者登入時抓取顯示規範資訊，並針對使用者的會話進行快取。</span><span class="sxs-lookup"><span data-stu-id="fa626-137">For the Windows shell, display specifier information is retrieved at user logon and cached for the user's session.</span></span> <span data-ttu-id="fa626-138">針對系統管理嵌入式管理單元，在載入嵌入式管理單元時，會抓取顯示規範資料，而且會在進程期間進行快取。</span><span class="sxs-lookup"><span data-stu-id="fa626-138">For the administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded and is cached for the duration of the process.</span></span> <span data-ttu-id="fa626-139">針對 Windows shell，這表示在使用者登出後重新登入後，顯示規範的變更會生效。</span><span class="sxs-lookup"><span data-stu-id="fa626-139">For the Windows shell, this means changes to display specifiers take effect after a user logs off and back on again.</span></span> <span data-ttu-id="fa626-140">系統管理嵌入式管理單元的變更會在嵌入式管理單元或主控台檔案重載時生效，也就是當您啟動新的主控台檔案實例或新的 Mmc.exe 實例並新增嵌入式管理單元時，會抓取最新的顯示規範資料。</span><span class="sxs-lookup"><span data-stu-id="fa626-140">For the administrative snap-ins, changes take effect when the snap-in or console file is reloaded, that is, if you start a new instance of the console file or new Mmc.exe instance and add the snap-in, the latest display specifier data is retrieved.</span></span>

 

<span data-ttu-id="fa626-141">如需詳細資訊，以及如何執行內容功能表延伸模組的程式碼範例，請參閱 [執行內容功能表 COM 物件的範例程式碼](example-code-for-implementation-of-the-context-menu-com-object.md)。</span><span class="sxs-lookup"><span data-stu-id="fa626-141">For more information, and a code example of how to implement a context menu extension, see [Example Code for Implementation of the Context Menu COM Object](example-code-for-implementation-of-the-context-menu-com-object.md).</span></span>

 

 