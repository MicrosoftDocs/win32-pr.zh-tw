---
title: 檔管理員
description: 檔管理員
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- '檔案管理員文字服務架構 (TSF) '
- TSF (文字服務架構) ，檔管理員
- 文字服務，檔管理員
- TSF 啟用應用程式，檔管理員
- 檔管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672143"
---
# <a name="document-manager"></a><span data-ttu-id="8104b-108">檔管理員</span><span class="sxs-lookup"><span data-stu-id="8104b-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="8104b-109">應用程式</span><span class="sxs-lookup"><span data-stu-id="8104b-109">Applications</span></span>

<span data-ttu-id="8104b-110">若要建立檔管理員物件，應用程式會呼叫 [ITfThreadMgr：： CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)。</span><span class="sxs-lookup"><span data-stu-id="8104b-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="8104b-111">應用程式會針對應用程式所維護的每個個別檔建立個別的檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="8104b-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="8104b-112">應用程式會使用 [檔案管理員] 來建立編輯內容、將內容加入內容堆疊，以及從內容堆疊中移除內容。</span><span class="sxs-lookup"><span data-stu-id="8104b-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="8104b-113">文字服務</span><span class="sxs-lookup"><span data-stu-id="8104b-113">Text Services</span></span>

<span data-ttu-id="8104b-114">文字服務永遠不會建立檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="8104b-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="8104b-115">相反地，文字服務會藉由呼叫 [ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)來取得目前使用中的檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="8104b-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="8104b-116">文字服務會使用檔管理員來取得堆疊頂端的內容。</span><span class="sxs-lookup"><span data-stu-id="8104b-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="8104b-117">文字服務也可以使用 [檔案管理員] 來建立自己的內容，並將它從內容堆疊中加入和移除。</span><span class="sxs-lookup"><span data-stu-id="8104b-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="8104b-118">這通常是在文字服務必須顯示某些強制回應使用者介面時完成，例如，當顯示單字清單讓使用者選取單字時。</span><span class="sxs-lookup"><span data-stu-id="8104b-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="8104b-119">當清單顯示時，文字服務會將自己的內容放在堆疊上。</span><span class="sxs-lookup"><span data-stu-id="8104b-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="8104b-120">當 word 清單關閉時，文字服務會將其內容從堆疊中移除。</span><span class="sxs-lookup"><span data-stu-id="8104b-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8104b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="8104b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8104b-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="8104b-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="8104b-123">ITfThreadMgr：： CreateDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="8104b-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="8104b-124">ITfThreadMgr：： GetFocus</span><span class="sxs-lookup"><span data-stu-id="8104b-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




