---
description: 本節包含用來控制 Tablet PC 輸入面板之外觀和行為的介面資訊。
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: 文字輸入面板介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195096"
---
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="77ee7-103">文字輸入面板介面</span><span class="sxs-lookup"><span data-stu-id="77ee7-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="77ee7-104">本節包含用來控制 Tablet PC 輸入面板之外觀和行為的介面資訊。</span><span class="sxs-lookup"><span data-stu-id="77ee7-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="77ee7-105">文字輸入面板介面不符合自動化規範。</span><span class="sxs-lookup"><span data-stu-id="77ee7-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="77ee7-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="77ee7-106">In This Section</span></span>



| <span data-ttu-id="77ee7-107">介面</span><span class="sxs-lookup"><span data-stu-id="77ee7-107">Interface</span></span>                                                                | <span data-ttu-id="77ee7-108">描述</span><span class="sxs-lookup"><span data-stu-id="77ee7-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77ee7-109">**IHandWrittenTextInsertion 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="77ee7-110">由應用程式的自訂文字專案程式碼用來將文字插入文字欄位和文字服務備份存放區。</span><span class="sxs-lookup"><span data-stu-id="77ee7-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="77ee7-111">**ITextInputPanel 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="77ee7-112">提供 Tablet PC 輸入面板的控制權。</span><span class="sxs-lookup"><span data-stu-id="77ee7-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="77ee7-113">**ITextInputPanelEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="77ee7-114">定義處理 [**ITextInputPanel 介面**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 事件的方法。</span><span class="sxs-lookup"><span data-stu-id="77ee7-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="77ee7-115">**ITextInputPanelRunInfo 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="77ee7-116">提供方法來判斷文字輸入面板目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="77ee7-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="77ee7-117">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="77ee7-118">可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。</span><span class="sxs-lookup"><span data-stu-id="77ee7-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="77ee7-119">**ITipAutocompleteProvider 介面**</span><span class="sxs-lookup"><span data-stu-id="77ee7-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="77ee7-120">管理文字輸入面板自動完成整合的應用程式端。</span><span class="sxs-lookup"><span data-stu-id="77ee7-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="77ee7-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="77ee7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ee7-122">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="77ee7-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




