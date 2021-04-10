---
title: 執行緒管理員
description: 執行緒管理員是 TSF 管理員的基礎元件。
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- '執行緒管理員文字服務架構 (TSF) '
- TSF (文字服務架構) ，執行緒管理員
- 文字服務，執行緒管理員
- 具有 TSF 功能的應用程式，執行緒管理員
- 執行緒管理員
- TSF 管理員
- 事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023723"
---
# <a name="thread-manager"></a><span data-ttu-id="bb767-110">執行緒管理員</span><span class="sxs-lookup"><span data-stu-id="bb767-110">Thread Manager</span></span>

<span data-ttu-id="bb767-111">執行緒管理員是 TSF 管理員的基礎元件。</span><span class="sxs-lookup"><span data-stu-id="bb767-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="bb767-112">執行緒管理員會執行與應用程式和文字服務 (用戶端) 相關的一般工作。</span><span class="sxs-lookup"><span data-stu-id="bb767-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="bb767-113">這些工作包括（但不限於）啟用和停用 TSF 文字服務、建立檔管理員，以及維護檔和輸入焦點之間的適當關聯性。</span><span class="sxs-lookup"><span data-stu-id="bb767-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="bb767-114">執行緒管理員是由 [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="bb767-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="bb767-115">TSF 管理員提供的大部分介面和物件都可以使用執行緒管理員介面提供的方法來取得。</span><span class="sxs-lookup"><span data-stu-id="bb767-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="bb767-116">應用程式</span><span class="sxs-lookup"><span data-stu-id="bb767-116">Applications</span></span>

<span data-ttu-id="bb767-117">應用程式會使用 CLSID TFThreadMgr 呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立執行緒管理員物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb767-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="bb767-118">文字服務</span><span class="sxs-lookup"><span data-stu-id="bb767-118">Text Services</span></span>

<span data-ttu-id="bb767-119">文字服務會取得 text service [ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) 方法中的執行緒管理員物件。</span><span class="sxs-lookup"><span data-stu-id="bb767-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="bb767-120">事件通知</span><span class="sxs-lookup"><span data-stu-id="bb767-120">Event Notifications</span></span>

<span data-ttu-id="bb767-121">執行緒管理員也會提供事件通知給用戶端。</span><span class="sxs-lookup"><span data-stu-id="bb767-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="bb767-122">在 TSF 中，事件通知是透過事件接收器（COM 物件）來提供。</span><span class="sxs-lookup"><span data-stu-id="bb767-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="bb767-123">為了接收來自執行緒管理員的通知，用戶端會執行 [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) 物件並安裝事件接收器。</span><span class="sxs-lookup"><span data-stu-id="bb767-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="bb767-124">藉由查詢 ITfSource 的執行緒管理員 \_ ，並使用 iid ITfThreadMgrEventSink 呼叫 [ITfSource：： AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) ，即可安裝事件接收器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb767-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb767-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb767-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb767-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="bb767-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="bb767-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="bb767-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="bb767-128">ITfTextInputProcessor：： Activate</span><span class="sxs-lookup"><span data-stu-id="bb767-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="bb767-129">ITfThreadMgrEventSink</span><span class="sxs-lookup"><span data-stu-id="bb767-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="bb767-130">ITfSource::AdviseSink</span><span class="sxs-lookup"><span data-stu-id="bb767-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 