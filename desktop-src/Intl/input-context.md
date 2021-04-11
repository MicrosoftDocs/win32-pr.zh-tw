---
description: '&\# 0034; 輸入內容&\# 0034; 是由 IMM 維護的內部結構。'
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: 輸入內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f1f83a397373e17a7d637b61a3232a3d72acde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849172"
---
# <a name="input-context"></a><span data-ttu-id="796e5-103">輸入內容</span><span class="sxs-lookup"><span data-stu-id="796e5-103">Input Context</span></span>

<span data-ttu-id="796e5-104">「輸入內容」是由 IMM 維護的內部結構。</span><span class="sxs-lookup"><span data-stu-id="796e5-104">An "input context" is an internal structure maintained by the IMM.</span></span> <span data-ttu-id="796e5-105">它包含 IME 狀態的相關資訊，並由 IME 視窗使用。</span><span class="sxs-lookup"><span data-stu-id="796e5-105">It contains information about the status of the IME and is used by IME windows.</span></span> <span data-ttu-id="796e5-106">根據預設，作業系統會建立並指派輸入內容到每個執行緒。</span><span class="sxs-lookup"><span data-stu-id="796e5-106">By default, the operating system creates and assigns an input context to each thread.</span></span> <span data-ttu-id="796e5-107">線上程中，此預設輸入內容是共用資源，並與每個新建立的視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="796e5-107">Within the thread, this default input context is a shared resource and is associated with each newly created window.</span></span>

<span data-ttu-id="796e5-108">若要在 IME 中取得或設定資訊，IME 感知的應用程式必須先取得與指定視窗相關聯之輸入內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="796e5-108">To retrieve or set information in the IME, an IME-aware application must first retrieve a handle to the input context associated with a specified window.</span></span> <span data-ttu-id="796e5-109">應用程式會使用 [**ImmGetCoNtext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) 函數來抓取控制碼。</span><span class="sxs-lookup"><span data-stu-id="796e5-109">The application retrieves the handle by using the [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) function.</span></span> <span data-ttu-id="796e5-110">它可以在後續呼叫的 IMM 函式中使用抓取的控制碼，以抓取和設定 IME 值，例如撰寫視窗樣式、撰寫樣式和狀態視窗位置。</span><span class="sxs-lookup"><span data-stu-id="796e5-110">It can use the retrieved handle in subsequent calls to the IMM functions to retrieve and set IME values, such as the composition window style, the composition style, and the status window position.</span></span> <span data-ttu-id="796e5-111">應用程式使用完內容之後，就必須使用 [**ImmReleaseCoNtext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) 函式來釋放內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-111">Once the application has finished using the context, it must release the context using the [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) function.</span></span>

<span data-ttu-id="796e5-112">由於預設輸入內容是共用資源，因此應用程式對其進行的任何變更都會套用至執行緒中的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="796e5-112">Because the default input context is a shared resource, any changes the application makes to it apply to all windows in the thread.</span></span> <span data-ttu-id="796e5-113">不過，應用程式可以藉由建立自己的輸入內容，並將它與執行緒的一或多個視窗產生關聯，來覆寫這個預設行為。</span><span class="sxs-lookup"><span data-stu-id="796e5-113">However, the application can override this default behavior by creating its own input context and associating it with one or more windows of the thread.</span></span> <span data-ttu-id="796e5-114">對應用程式特定輸入內容所做的變更只會套用至與內容相關聯的視窗。</span><span class="sxs-lookup"><span data-stu-id="796e5-114">The changes made to an application-specific input context apply only to the windows associated with the context.</span></span>

<span data-ttu-id="796e5-115">您的應用程式可以使用 [**ImmCreateCoNtext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) 函數來建立輸入內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-115">Your application can create an input context by using the [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) function.</span></span> <span data-ttu-id="796e5-116">若要將內容指派給視窗，應用程式會呼叫 [**ImmAssociateCoNtext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="796e5-116">To assign the context to a window, the application calls the [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) function.</span></span> <span data-ttu-id="796e5-117">此函式會將控制碼傳回至先前關聯的輸入內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-117">This function returns a handle to the previously associated input context.</span></span> <span data-ttu-id="796e5-118">如果應用程式尚未與視窗建立關聯的輸入內容，傳回的控制碼會是預設的輸入內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-118">If the application has not already associated an input context with the window, the returned handle is for the default input context.</span></span> <span data-ttu-id="796e5-119">一般來說，當不再需要自訂的輸入內容時，應用程式會儲存此控制碼，並在稍後使用視窗重新關聯它。</span><span class="sxs-lookup"><span data-stu-id="796e5-119">Typically, the application saves this handle and later reassociates it with the window when the customized input context is no longer needed.</span></span>

<span data-ttu-id="796e5-120">一旦輸入內容與視窗相關聯之後，作業系統會在視窗啟動時自動選取該內容，並接收輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="796e5-120">Once an input context is associated with a window, the operating system automatically selects that context when the window is activated and receives the input focus.</span></span> <span data-ttu-id="796e5-121">輸入內容中的樣式和其他資訊會影響該視窗的後續鍵盤輸入，以判斷 IME 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="796e5-121">The style and other information in the input context affects subsequent keyboard input for that window, determining how the IME operates.</span></span>

<span data-ttu-id="796e5-122">您的應用程式必須在結束之前終結任何自訂的輸入內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-122">Your application must destroy any customized input context before it terminates.</span></span> <span data-ttu-id="796e5-123">首先，應用程式會使用 [**ImmAssociateCoNtext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) 函式，從線上程中與 windows 建立的任何關聯中移除輸入內容。</span><span class="sxs-lookup"><span data-stu-id="796e5-123">First, the application removes the input context from any association it has made with windows in the thread by using the [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) function.</span></span> <span data-ttu-id="796e5-124">然後，它會呼叫 [**ImmDestroyCoNtext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="796e5-124">Then, it calls the [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="796e5-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="796e5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="796e5-126">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="796e5-126">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



