---
description: 如何從沒有關聯的檔案類型的 [開啟檔案] 對話方塊中排除應用程式。
title: 如何從非關聯檔案類型的 [開啟檔案] 對話方塊中排除應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571241"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="93ce7-103">如何從非關聯檔案類型的 [開啟檔案] 對話方塊中排除應用程式</span><span class="sxs-lookup"><span data-stu-id="93ce7-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="93ce7-104">當使用者嘗試開啟的檔案不是任何已註冊檔案類型的成員時 (也就是) 未知的檔案類型，或是當使用者從檔案的快捷方式功能表中選取 [ **開啟檔案** ] 或 **[開啟檔案-> 選擇預設程式** ] 時，命令介面會顯示一個子功能表或對話方塊，讓使用者能夠指定用來開啟檔案的程式。</span><span class="sxs-lookup"><span data-stu-id="93ce7-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="93ce7-105">根據預設，任何註冊為 **HKEY \_ 類別 \_ 根** 應用程式子機碼的應用程式， \\ 都會顯示在 [**開啟檔案**] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="93ce7-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="93ce7-106">無論應用程式是否已註冊來處理檔案類型，這些應用程式都會在 **開啟檔案** 中顯示。</span><span class="sxs-lookup"><span data-stu-id="93ce7-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="93ce7-107">若要防止應用程式在應用程式不應該或無法用來開啟特定檔案類型時出現在 [ **開啟檔案** ] 對話方塊中，請使用本主題中所述的兩種技術之一。</span><span class="sxs-lookup"><span data-stu-id="93ce7-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="93ce7-108">指示</span><span class="sxs-lookup"><span data-stu-id="93ce7-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="93ce7-109">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="93ce7-109">Step 1:</span></span>

<span data-ttu-id="93ce7-110">將 NoOpenWith 專案新增至應用程式的子機碼。</span><span class="sxs-lookup"><span data-stu-id="93ce7-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="93ce7-111">當應用程式使用檔案類型時，Windows 會記錄該資訊來建立 **建議的程式** 清單。</span><span class="sxs-lookup"><span data-stu-id="93ce7-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="93ce7-112">這份清單會顯示在 **開啟檔案** 子功能表中，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="93ce7-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![顯示快捷方式功能表的螢幕擷取畫面，其中顯示 [開啟方式] 子功能表](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="93ce7-114">這些建議的應用程式也會顯示在 [**開啟檔案**] 對話方塊的 [**建議的程式**] 部分中，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="93ce7-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![具有建議程式之 [開啟方式] 對話方塊的螢幕擷取畫面](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="93ce7-116">如果應用程式已在檔案類型的 [OpenWithList](fa-file-types.md) 或 OpenWithProgIDs 中註冊本身，即使已設定 NoOpenWith 專案，也會出現在 [ **建議的程式** ] 清單中。</span><span class="sxs-lookup"><span data-stu-id="93ce7-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="93ce7-117">此外，請記住，不論是否在建議的程式清單中提供應用程式，使用者都可以手動流覽至任何可執行檔。</span><span class="sxs-lookup"><span data-stu-id="93ce7-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="93ce7-118">應用程式可以在應用程式的子機碼底下指定 NoOpenWith 值，以停用此追蹤。</span><span class="sxs-lookup"><span data-stu-id="93ce7-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="93ce7-119">NoOpenWith 專案是空的 **REG \_ SZ** 值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="93ce7-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="93ce7-120">設定 NoOpenWith 專案也會有下列影響：</span><span class="sxs-lookup"><span data-stu-id="93ce7-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="93ce7-121">防止將檔案釘選到應用程式的捷徑清單透過拖放，除非應用程式是特別註冊來處理該檔案類型。</span><span class="sxs-lookup"><span data-stu-id="93ce7-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="93ce7-122">防止 [一般檔案] 對話方塊和 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 函式的任何呼叫將任何檔案新增至應用程式的捷徑清單，除非應用程式已特別註冊來處理該檔案類型。</span><span class="sxs-lookup"><span data-stu-id="93ce7-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="93ce7-123">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="93ce7-123">Step 2:</span></span>

<span data-ttu-id="93ce7-124">避免應用程式出現在 [ **開啟檔案** ] 對話方塊中的第二種方式，是使用 **SupportedTypes** 子機碼來明確列出應用程式可以開啟的檔案類型延伸模組。</span><span class="sxs-lookup"><span data-stu-id="93ce7-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="93ce7-125">這可防止應用程式在無法開啟的檔案類型的 [ **開啟檔案** ] 對話方塊中出現。</span><span class="sxs-lookup"><span data-stu-id="93ce7-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="93ce7-126">它也會讓應用程式出現在 **建議的程式** 清單中，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="93ce7-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="93ce7-127">如果應用程式可以將檔案儲存為特定檔案類型，但無法開啟該檔案類型，這個方法特別有用。</span><span class="sxs-lookup"><span data-stu-id="93ce7-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="93ce7-128">應用程式也應該 \_ 在呼叫 [**儲存**] 對話方塊時，透過 [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions)設定 FOS DONTADDTORECENT 旗標。</span><span class="sxs-lookup"><span data-stu-id="93ce7-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="93ce7-129">這會讓專案不會加入至捷徑清單的 **最新** 或 **經常** 的部分。</span><span class="sxs-lookup"><span data-stu-id="93ce7-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="93ce7-130">它也會封鎖在 [OpenWithList](fa-file-types.md)下追蹤應用程式。</span><span class="sxs-lookup"><span data-stu-id="93ce7-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="93ce7-131">每個支援的延伸模組都會新增為 **SupportedTypes** 子機碼底下的專案，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="93ce7-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="93ce7-132">專案的類型為 **REG \_ SZ** 或 **reg \_ Null**，沒有相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="93ce7-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="93ce7-133">如果提供 **SupportedTypes** 子機碼，則只有具有這些副檔名的檔案才有資格釘選到應用程式的捷徑清單，或在應用程式 **最近** 或 **經常** 的目的地清單中進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="93ce7-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="93ce7-134">NoOpenWith 專案會覆寫 **SupportedTypes** 子機碼，並在 [ **開啟檔案** ] 對話方塊中隱藏應用程式。</span><span class="sxs-lookup"><span data-stu-id="93ce7-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
