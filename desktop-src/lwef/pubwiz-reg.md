---
title: 註冊服務
description: 若要將您的服務加入至 [Web 發佈嚮導] 或 [線上列印順序] Wizard 中的提供者清單，您必須將適當的金鑰和其值新增至 Windows 登錄。
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- 註冊、服務
- Web 發佈嚮導，註冊
- 線上列印訂購嚮導，註冊
- 註冊，Web 發佈嚮導
- 註冊，線上列印訂購嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196151"
---
# <a name="registering-a-service"></a><span data-ttu-id="f46d2-108">註冊服務</span><span class="sxs-lookup"><span data-stu-id="f46d2-108">Registering a Service</span></span>

<span data-ttu-id="f46d2-109">若要將您的服務加入至 [Web 發佈嚮導] 或 [線上列印順序] Wizard 中的提供者清單，您必須將適當的金鑰和其值新增至 Windows 登錄。</span><span class="sxs-lookup"><span data-stu-id="f46d2-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="f46d2-110">必要的索引鍵和值</span><span class="sxs-lookup"><span data-stu-id="f46d2-110">Required Keys and Values</span></span>

<span data-ttu-id="f46d2-111">若要將您的服務加入至 Web 發佈嚮導的提供者清單，請新增如下所示的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f46d2-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="f46d2-112">若要將您的服務新增至線上列印訂購嚮導的提供者清單，請新增如下所示的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f46d2-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="f46d2-113">每個值都是 REG SZ 型別的字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f46d2-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="f46d2-114">提供其資料，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="f46d2-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="f46d2-115">值名稱</span><span class="sxs-lookup"><span data-stu-id="f46d2-115">Value Name</span></span>     | <span data-ttu-id="f46d2-116">說明</span><span class="sxs-lookup"><span data-stu-id="f46d2-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46d2-117">>iconpath</span><span class="sxs-lookup"><span data-stu-id="f46d2-117">IconPath</span></span>       | <span data-ttu-id="f46d2-118">圖示檔案的完整路徑，包括檔案名。</span><span class="sxs-lookup"><span data-stu-id="f46d2-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f46d2-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="f46d2-119">DisplayName</span></span>    | <span data-ttu-id="f46d2-120">在嚮導的 [提供者] 清單中，為您的服務顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="f46d2-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f46d2-121">Description</span><span class="sxs-lookup"><span data-stu-id="f46d2-121">Description</span></span>    | <span data-ttu-id="f46d2-122">您服務的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f46d2-122">A short description for your service.</span></span> <span data-ttu-id="f46d2-123">此描述也會顯示在您的服務名稱正下方的 wizard 提供者清單中。</span><span class="sxs-lookup"><span data-stu-id="f46d2-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f46d2-124">Href</span><span class="sxs-lookup"><span data-stu-id="f46d2-124">HREF</span></span>           | <span data-ttu-id="f46d2-125">服務第一頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="f46d2-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f46d2-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="f46d2-126">SupportedTypes</span></span> | <span data-ttu-id="f46d2-127">您的服務所支援的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="f46d2-127">The file types supported by your service.</span></span> <span data-ttu-id="f46d2-128">例如， *\* .jpg*。</span><span class="sxs-lookup"><span data-stu-id="f46d2-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="f46d2-129">只要指定特定檔案類型，您的服務就只會在選取這些檔案類型時出現。</span><span class="sxs-lookup"><span data-stu-id="f46d2-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="f46d2-130">如果選取了多個檔案類型，如果您的服務支援這些檔案類型的任何一種，則會出現您的服務。</span><span class="sxs-lookup"><span data-stu-id="f46d2-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="f46d2-131">如果您想要指定多個檔案類型，請在清單中以分號分隔它們。</span><span class="sxs-lookup"><span data-stu-id="f46d2-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="f46d2-132">例如， *\* .jpg; \* 。bmp*。</span><span class="sxs-lookup"><span data-stu-id="f46d2-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="f46d2-133">以下是名為 "MyProvider" 之相片處理服務的完整範例。</span><span class="sxs-lookup"><span data-stu-id="f46d2-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="f46d2-134">呼叫服務的 URL 時，會將兩個值新增至 URL 的結尾，也就是 lcid 和 langid。</span><span class="sxs-lookup"><span data-stu-id="f46d2-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="f46d2-135">例如，上述範例的 URL 字串可能是 HTTPs： \/ /www.MyProvider.com/Intro.htm？ lcid = 1033&langid = 1033。</span><span class="sxs-lookup"><span data-stu-id="f46d2-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="f46d2-136">這些變數會用於語言和當地語系化資訊。</span><span class="sxs-lookup"><span data-stu-id="f46d2-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="f46d2-137">**lcid** 用來通知伺服器用戶端的國家/地區和語言設定。</span><span class="sxs-lookup"><span data-stu-id="f46d2-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="f46d2-138">它不會用來判斷用戶端 UI 的語言，而是用來判斷貨幣、日期和時間，以及其他特定區域資料的正確格式。</span><span class="sxs-lookup"><span data-stu-id="f46d2-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="f46d2-139">**langid** 用來通知伺服器用戶端的預設語言設定，讓它可以在 UI 中使用適當的語言。</span><span class="sxs-lookup"><span data-stu-id="f46d2-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




