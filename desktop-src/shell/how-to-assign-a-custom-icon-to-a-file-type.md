---
description: 您必須將自訂圖示指派給檔案類型，以提供視覺指示給該檔案類型的使用者，或與檔案類型相關聯的應用程式。
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: 如何將自訂圖示指派給檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973181"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="a27db-103">如何將自訂圖示指派給檔案類型</span><span class="sxs-lookup"><span data-stu-id="a27db-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="a27db-104">當沒有任何自訂預設圖示指派給檔案類型時，桌面和 Windows 檔案總管會以一般預設圖示來顯示該類型的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="a27db-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="a27db-105">例如，下列螢幕擷取畫面顯示與 MyDocs4. myp 檔案搭配使用的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="a27db-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![預設圖示的螢幕擷取畫面](images/icon.png)

<span data-ttu-id="a27db-107">雖然在此螢幕擷取畫面中顯示的所有檔案都是簡單的文字檔，但只有 MyDocs4 會顯示 Windows 預設圖示。</span><span class="sxs-lookup"><span data-stu-id="a27db-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="a27db-108">這是因為 .txt 副檔名是具有自訂預設圖示的已註冊檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a27db-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="a27db-109">下列螢幕擷取畫面顯示已指派給 myp 檔案類型的自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="a27db-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![myp 檔案自訂圖示的螢幕擷取畫面](images/context4.png)

> [!Note]  
> <span data-ttu-id="a27db-111">您也可以在應用程式特定的基礎上指派圖示。</span><span class="sxs-lookup"><span data-stu-id="a27db-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="a27db-112">指示</span><span class="sxs-lookup"><span data-stu-id="a27db-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a27db-113">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="a27db-113">Step 1:</span></span>

<span data-ttu-id="a27db-114">在下列兩個位置的其中一個位置建立名為 **DefaultIcon** 的子機碼：</span><span class="sxs-lookup"><span data-stu-id="a27db-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="a27db-115">針對檔案類型指派， **HKEY 類別的 \_ \_ 根目錄** \\ *副檔名*</span><span class="sxs-lookup"><span data-stu-id="a27db-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="a27db-116">針對應用程式指派， **HKEY \_ 類別 \_ 根目錄** \\ *ProgID*</span><span class="sxs-lookup"><span data-stu-id="a27db-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="a27db-117">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="a27db-117">Step 2:</span></span>

<span data-ttu-id="a27db-118">指派 **DefaultIcon** 子機碼為 **REG \_ SZ** 類型的預設值，指定包含圖示之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a27db-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="a27db-119">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="a27db-119">Step 3:</span></span>

<span data-ttu-id="a27db-120">呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 函數，以通知 Shell 更新其圖示快取。</span><span class="sxs-lookup"><span data-stu-id="a27db-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="a27db-121">備註</span><span class="sxs-lookup"><span data-stu-id="a27db-121">Remarks</span></span>

<span data-ttu-id="a27db-122">下列範例會詳細說明檔案類型圖示指派所需的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="a27db-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="a27db-123">副檔名是與應用程式相關聯，但圖示指派是在副檔名本身，因此相關聯的應用程式不會指定預設圖示。</span><span class="sxs-lookup"><span data-stu-id="a27db-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="a27db-124">下列範例顯示應用程式圖示指派所需的登錄專案詳細觀點。</span><span class="sxs-lookup"><span data-stu-id="a27db-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="a27db-125">Myp 副檔名會先與 Myprogram.exe. 1 應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="a27db-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="a27db-126">接著會將自訂預設圖示指派給 Myprogram.exe. 1 ProgID 子機碼。</span><span class="sxs-lookup"><span data-stu-id="a27db-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="a27db-127">任何包含圖示的檔案都是可接受的，包括 .ico、.exe 和 .dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="a27db-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="a27db-128">如果檔案中有一個以上的圖示，路徑後面應該接著逗號，再接著圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="a27db-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a27db-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a27db-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a27db-130">檔案類型</span><span class="sxs-lookup"><span data-stu-id="a27db-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



