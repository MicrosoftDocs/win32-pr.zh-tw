---
title: 用戶端識別碼
description: 用戶端識別碼
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- 文字服務架構 (TSF) 、用戶端識別碼
- TSF (文字服務架構) 、用戶端識別碼
- 文字服務、用戶端識別碼
- 啟用 TSF 的應用程式，用戶端識別碼
- 用戶端識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de15b208d2fbc6c6ea5c2a1114eb5cb23ff12ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932031"
---
# <a name="client-identifiers"></a><span data-ttu-id="ada29-108">用戶端識別碼</span><span class="sxs-lookup"><span data-stu-id="ada29-108">Client Identifiers</span></span>

## <a name="applications"></a><span data-ttu-id="ada29-109">應用程式</span><span class="sxs-lookup"><span data-stu-id="ada29-109">Applications</span></span>

<span data-ttu-id="ada29-110">應用程式會藉由呼叫 [ITfThreadMgr：： Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)來取得其用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="ada29-110">An application obtains its client identifier by calling [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span>

## <a name="text-services"></a><span data-ttu-id="ada29-111">文字服務</span><span class="sxs-lookup"><span data-stu-id="ada29-111">Text Services</span></span>

<span data-ttu-id="ada29-112">當呼叫 text service [ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) 方法時，文字服務會取得其用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="ada29-112">A text service obtains its client identifier when the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method is called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ada29-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="ada29-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada29-114">ITfThreadMgr：： Activate</span><span class="sxs-lookup"><span data-stu-id="ada29-114">ITfThreadMgr::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[<span data-ttu-id="ada29-115">ITfTextInputProcessor：： Activate</span><span class="sxs-lookup"><span data-stu-id="ada29-115">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




