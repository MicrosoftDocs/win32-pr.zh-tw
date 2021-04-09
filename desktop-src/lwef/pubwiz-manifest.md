---
title: 使用傳送資訊清單
description: Web 發佈嚮導和線上列印順序 Wizard 會使用傳輸資訊清單來傳達用戶端電腦與伺服器網站之間資料傳輸的詳細資料。
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Web 發佈嚮導，傳送資訊清單
- 線上列印訂購嚮導，傳送資訊清單
- 傳送資訊清單
- manifest
- window. external、transfer 資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842275"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="41082-108">使用傳送資訊清單</span><span class="sxs-lookup"><span data-stu-id="41082-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="41082-109">Web 發佈嚮導和線上列印順序 Wizard 會使用傳輸資訊清單來傳達用戶端電腦與伺服器網站之間資料傳輸的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41082-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="41082-110">傳送資訊清單的用途</span><span class="sxs-lookup"><span data-stu-id="41082-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="41082-111">傳送資訊清單描述傳輸中牽涉到的檔案，包括目的地階層和檔案中繼資料等詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41082-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="41082-112">伺服器端腳本可以修改資訊清單，方法是從清單中移除不適當的檔案，並新增有關如何以及應該如何傳送檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="41082-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="41082-113">資訊清單會公開為屬性 **視窗。 external. property ( "TransferManifest" )**，XML 檔物件模型 (DOM) 檔。</span><span class="sxs-lookup"><span data-stu-id="41082-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="41082-114">如需有關 XML DOM 的詳細資訊，請參閱 [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85))的 MSDN 檔。</span><span class="sxs-lookup"><span data-stu-id="41082-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="41082-115">傳送資訊清單的最上層組織如下所示：</span><span class="sxs-lookup"><span data-stu-id="41082-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="41082-116">伺服器端 HTML 網頁可以使用資訊清單中的節點來取得要複製之檔案的特定資訊，然後據以修改服務的 UI。</span><span class="sxs-lookup"><span data-stu-id="41082-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="41082-117">比方說，相片列印網站可能會使用此資訊來顯示所選影像的縮圖，而儲存場所可能會使用此資訊，以確保該使用者有足夠的儲存空間可供使用。</span><span class="sxs-lookup"><span data-stu-id="41082-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="41082-118">如需有關傳送資訊清單節點和屬性的完整資訊，請參閱 [傳送資訊清單架構](/windows/desktop/shell/interfaces)。</span><span class="sxs-lookup"><span data-stu-id="41082-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="41082-119">傳送資訊清單架構會以開啟的模型的形式寫入，因此不會在架構中明確定義的元素可能會出現在傳送資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="41082-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="41082-120">因此，提供者網站可能會新增專屬專案以供自己使用，而不會干擾資訊清單的有效性。</span><span class="sxs-lookup"><span data-stu-id="41082-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="41082-121">架構也會定義成不限制元素的順序。</span><span class="sxs-lookup"><span data-stu-id="41082-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="41082-122">每次選擇新的提供者時，就會重新建立資訊清單，讓提供者有機會將網站資訊儲存在資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="41082-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="41082-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="41082-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41082-124">傳送資訊清單架構</span><span class="sxs-lookup"><span data-stu-id="41082-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 