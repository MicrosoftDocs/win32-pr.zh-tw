---
title: IAgent 載入
description: IAgent 載入
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933217"
---
# <a name="iagentload"></a><span data-ttu-id="7b52d-103">IAgent：： Load</span><span class="sxs-lookup"><span data-stu-id="7b52d-103">IAgent::Load</span></span>

<span data-ttu-id="7b52d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7b52d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="7b52d-105">將字元載入至 [**字元**](./iagent.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="7b52d-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="7b52d-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="7b52d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7b52d-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="7b52d-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="7b52d-108">必須是下列其中一項的 variant 資料類型：</span><span class="sxs-lookup"><span data-stu-id="7b52d-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7b52d-109">*filespec*</span><span class="sxs-lookup"><span data-stu-id="7b52d-109">*filespec*</span></span> | <span data-ttu-id="7b52d-110">指定字元之定義檔的本機檔案位置。</span><span class="sxs-lookup"><span data-stu-id="7b52d-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="7b52d-111">*URL*</span><span class="sxs-lookup"><span data-stu-id="7b52d-111">*URL*</span></span>      | <span data-ttu-id="7b52d-112">字元定義檔的 HTTP 位址。</span><span class="sxs-lookup"><span data-stu-id="7b52d-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="7b52d-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="7b52d-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="7b52d-114">接收字元識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="7b52d-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="7b52d-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="7b52d-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="7b52d-116">接收 [**載入**](load-method.md) 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="7b52d-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="7b52d-117">您可以從 Microsoft Agent 子目錄中指定相對路徑來載入字元， (不含冒號或開頭斜線字元) 。</span><span class="sxs-lookup"><span data-stu-id="7b52d-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="7b52d-118">這個前置詞會在當地語系化的% windows% msagent 目錄) 中，使用代理程式的字元目錄 (路徑 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7b52d-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="7b52d-119">您也可以使用相對位址，在代理程式的 [字元] 目錄中指定您自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="7b52d-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="7b52d-120">您無法將相同的字元從單一連接載入相同的字元 (一次以上的字元) 。</span><span class="sxs-lookup"><span data-stu-id="7b52d-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="7b52d-121">同樣地，您不能同時從單一連接載入預設字元和其他字元，因為預設字元可能與另一個字元相同。</span><span class="sxs-lookup"><span data-stu-id="7b52d-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="7b52d-122">不過，您可以使用 CoCreateInstance) 建立另一個連接 (，然後載入相同的字元。</span><span class="sxs-lookup"><span data-stu-id="7b52d-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="7b52d-123">Microsoft 代理程式的資料提供者支援載入以單一結構化檔案 ( 儲存的字元資料。ACS) 搭配字元資料和動畫資料，或個別的字元資料 (。ACF) 和動畫 (。ACA) 檔。</span><span class="sxs-lookup"><span data-stu-id="7b52d-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="7b52d-124">一般而言，使用單一結構化。ACS 檔案來載入儲存在本機磁片磁碟機或網路上的字元，並使用傳統的檔案通訊協定（例如 UNC 路徑)  (）進行存取。</span><span class="sxs-lookup"><span data-stu-id="7b52d-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="7b52d-125">使用不同的。ACF 和。當您想要從使用 HTTP 通訊協定存取它們的遠端網站個別載入動畫檔案時，ACA 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b52d-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="7b52d-126">出於.ACS 檔案，使用 [**Load**](load-method.md) 方法可提供存取字元的動畫;載入之後，您可以使用 [**Play**](play-method.md) 方法來建立字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="7b52d-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="7b52d-127">出於.ACF 檔案，您也可以使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來載入動畫資料。</span><span class="sxs-lookup"><span data-stu-id="7b52d-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="7b52d-128">**載入** 方法不支援下載。來自 HTTP 網站的 ACS 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b52d-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="7b52d-129">載入字元不會自動顯示字元。</span><span class="sxs-lookup"><span data-stu-id="7b52d-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="7b52d-130">先使用 [**Show**](show-method.md) 方法讓字元變成可見。</span><span class="sxs-lookup"><span data-stu-id="7b52d-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 