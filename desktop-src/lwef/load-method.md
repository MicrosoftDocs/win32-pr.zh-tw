---
title: 載入方法
description: 載入方法
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966854"
---
# <a name="load-method"></a><span data-ttu-id="690c8-103">載入方法</span><span class="sxs-lookup"><span data-stu-id="690c8-103">Load Method</span></span>

<span data-ttu-id="690c8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="690c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="690c8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="690c8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="690c8-106">將字元載入至 [**字元**](/windows/desktop/lwef/the-characters-object) 集合。</span><span class="sxs-lookup"><span data-stu-id="690c8-106">Loads a character into the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="690c8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="690c8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="690c8-108">\*代理程式 ***。字元。 Load "*** CharacterID \* \* *"，* \*  *提供者*</span><span class="sxs-lookup"><span data-stu-id="690c8-108">*agent ***.Characters.Load "*** CharacterID\*\*\*",*\* *Provider*</span></span>



| <span data-ttu-id="690c8-109">部分</span><span class="sxs-lookup"><span data-stu-id="690c8-109">Part</span></span>          | <span data-ttu-id="690c8-110">描述</span><span class="sxs-lookup"><span data-stu-id="690c8-110">Description</span></span>                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="690c8-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="690c8-111">*CharacterID*</span></span> | <span data-ttu-id="690c8-112">必要。</span><span class="sxs-lookup"><span data-stu-id="690c8-112">Required.</span></span> <span data-ttu-id="690c8-113">您將用來參考要載入之字元資料的字串值。</span><span class="sxs-lookup"><span data-stu-id="690c8-113">A string value that you will use to refer to the character data to be loaded.</span></span>                                                                                                                                                  |
| <span data-ttu-id="690c8-114">*提供者*</span><span class="sxs-lookup"><span data-stu-id="690c8-114">*Provider*</span></span>    | <span data-ttu-id="690c8-115">必要。</span><span class="sxs-lookup"><span data-stu-id="690c8-115">Required.</span></span> <span data-ttu-id="690c8-116">必須是下列其中一項的 variant 資料類型： **Filespec** 指定字元之定義檔的本機檔案位置。</span><span class="sxs-lookup"><span data-stu-id="690c8-116">A variant data type that must be one of the following: **Filespec** The local file location of the specified character's definition file.</span></span> <br/> <span data-ttu-id="690c8-117">**URL** 字元定義檔的 HTTP 位址。</span><span class="sxs-lookup"><span data-stu-id="690c8-117">**URL** The HTTP address for the character's definition file.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="690c8-118">備註</span><span class="sxs-lookup"><span data-stu-id="690c8-118">Remarks</span></span>

<span data-ttu-id="690c8-119">您可以從代理程式子目錄中指定相對路徑來載入字元， (不含冒號或開頭斜線字元) 。</span><span class="sxs-lookup"><span data-stu-id="690c8-119">You can load characters from the Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="690c8-120">這會在當地語系化的 Windows msagent 目錄) 中，使用代理程式的字元目錄 (路徑 \\ 。</span><span class="sxs-lookup"><span data-stu-id="690c8-120">This prefixes the path with Agent's characters directory (located in the localized Windows\\msagent directory).</span></span> <span data-ttu-id="690c8-121">例如，指定下列內容會從代理程式的字元目錄載入瓶精靈。</span><span class="sxs-lookup"><span data-stu-id="690c8-121">For example, specifying the following would load Genie.acs from Agent's Chars directory:</span></span>


```
   Agent.Character.Load "genie", "genie.acs"
```



<span data-ttu-id="690c8-122">您也可以在代理程式的 [字元] 目錄中指定自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="690c8-122">You can also specify your own directory in Agent's Chars directory.</span></span>


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



<span data-ttu-id="690c8-123">您可以將目前設定為目前使用者預設字元的字元載入，方法是不要將路徑包含為 **load** 方法的第二個參數。</span><span class="sxs-lookup"><span data-stu-id="690c8-123">You can load the character currently set as the current user's default character by not including a path as the second parameter of the **Load** method.</span></span>


```
   Agent.Character.Load "character"
```



<span data-ttu-id="690c8-124">您無法從控制項的單一實例，將相同的字元 (具有相同 GUID 的字元) 一次以上。</span><span class="sxs-lookup"><span data-stu-id="690c8-124">You cannot load the same character (a character having the same GUID) more than once from a single instance of the control.</span></span> <span data-ttu-id="690c8-125">同樣地，您無法同時從控制項的單一實例載入預設字元和其他字元，因為預設字元可能與其他字元相同。</span><span class="sxs-lookup"><span data-stu-id="690c8-125">Similarly, you cannot load the default character and other characters at the same time from a single instance of the control because the default character could be the same as the other character.</span></span> <span data-ttu-id="690c8-126">如果您嘗試這麼做，伺服器會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="690c8-126">If you attempt to do this, the server raises an error.</span></span> <span data-ttu-id="690c8-127">不過，您可以建立 Agent 控制項的另一個實例，並載入相同的字元。</span><span class="sxs-lookup"><span data-stu-id="690c8-127">However, you can create another instance of the Agent control and load the same character.</span></span>

<span data-ttu-id="690c8-128">Microsoft Agent Data Provider 支援載入儲存為單一結構化檔案 ( 的字元資料。ACS) 搭配字元資料和動畫資料，或以個別的字元資料 (。ACF) 和動畫 (。ACA) 檔。</span><span class="sxs-lookup"><span data-stu-id="690c8-128">The Microsoft Agent Data Provider supports loading character data stored either as a single structured file (.ACS) with character data and animation data together or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="690c8-129">使用單一結構化。ACS 檔案來載入儲存在本機磁片或網路上的字元，並使用傳統的檔案通訊協定來存取， (例如 UNC 路徑) 。</span><span class="sxs-lookup"><span data-stu-id="690c8-129">Use the single structured .ACS file to load a character that is stored on a local disk or network and accessed using a conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="690c8-130">使用不同的。ACF 和。當您想要從使用 HTTP 通訊協定來存取它們的遠端網站個別載入動畫檔案時，ACA 檔案。</span><span class="sxs-lookup"><span data-stu-id="690c8-130">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using the HTTP protocol.</span></span>

<span data-ttu-id="690c8-131">出於.使用 **Load** 方法的 ACS 檔案可存取字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="690c8-131">For .ACS files, using the **Load** method provides access to a character's animations.</span></span> <span data-ttu-id="690c8-132">出於.ACF 檔案，您也可以使用 [**Get**](get-method.md) 方法來載入動畫資料。</span><span class="sxs-lookup"><span data-stu-id="690c8-132">For .ACF files, you also use the [**Get**](get-method.md) method to load animation data.</span></span> <span data-ttu-id="690c8-133">**載入** 方法不支援下載。來自 HTTP 網站的 ACS 檔案。</span><span class="sxs-lookup"><span data-stu-id="690c8-133">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="690c8-134">載入字元不會自動顯示字元。</span><span class="sxs-lookup"><span data-stu-id="690c8-134">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="690c8-135">先使用 [**Show**](show-method.md) 方法讓字元變成可見。</span><span class="sxs-lookup"><span data-stu-id="690c8-135">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

<span data-ttu-id="690c8-136">如果您使用 **load** 方法載入儲存在本機電腦上的字元檔，則呼叫會失敗;例如，由於找不到檔案，因此 Agent 會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="690c8-136">If you use the **Load** method to load a character file stored on the local machine and the call fails; for example, because the file is not found, Agent raises an error.</span></span> <span data-ttu-id="690c8-137">您可以使用程式設計語言的支援，提供錯誤處理常式來攔截和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="690c8-137">You can use the support in your programming language to provide an error handling routine to catch and process the error.</span></span>


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



<span data-ttu-id="690c8-138">您也可以將 [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) 設定為 **False**、宣告物件，並將 **載入** 要求指派給它，以處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="690c8-138">You can also handle the error by setting [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) to **False**, declaring a object, and assigning the **Load** request to it.</span></span> <span data-ttu-id="690c8-139">然後，遵循具有檢查 [**要求**](/windows/desktop/lwef/the-request-object)物件狀態的語句，來進行 **Load** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="690c8-139">Then follow the **Load** call with a statement that checks the status of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



<span data-ttu-id="690c8-140">如果您載入的字元不是本機，例如，您也可以使用 HTTP 通訊協定，藉由將 [**要求**](/windows/desktop/lwef/the-request-object)物件指派給 **load** 方法來檢查 **載入** 失敗。</span><span class="sxs-lookup"><span data-stu-id="690c8-140">If you load a character that is not local; for example, using HTTP protocol, you can also check for a **Load** failure by assigning a [**Request**](/windows/desktop/lwef/the-request-object) object to the **Load** method.</span></span> <span data-ttu-id="690c8-141">不過，因為這種載入字元的方法會以非同步方式處理，所以請檢查其在 [**RequestComplete**](requestcomplete-event.md) 事件中的狀態。</span><span class="sxs-lookup"><span data-stu-id="690c8-141">However, because this method of loading a character is handled asynchronously, check its status in the [**RequestComplete**](requestcomplete-event.md) event.</span></span> <span data-ttu-id="690c8-142">這項技術將無法使用 UNC 通訊協定載入字元，因為會以同步方式處理 **Load** 方法。</span><span class="sxs-lookup"><span data-stu-id="690c8-142">This technique will not work loading a character using the UNC protocol because the **Load** method is processed synchronously.</span></span>

 

