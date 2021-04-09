---
description: COM + 如何修改傳回值
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: COM + 如何修改傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110917"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="3e976-103">COM + 如何修改傳回值</span><span class="sxs-lookup"><span data-stu-id="3e976-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="3e976-104">COM + 絕不會變更指出失敗的 **HRESULT** 傳回值，例如 e 非 \_ 預期或 e \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="3e976-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="3e976-105">不過，當使用 COM + 功能的物件傳回 **HRESULT** 值，指出成功 (（例如 s \_ OK、s \_ FALSE 或 >aad-userreadusingalternativesecurityid-noerror) ）時，com + 有時會在傳回給呼叫端之前將 **hresult** 轉換成 com + 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3e976-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="3e976-106">例如，當應用程式在 \_ 呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)之後傳回 S OK 時，如果物件是無法認可之交易的根，則 **HRESULT** 會轉換成內容 \_ E \_ 中止。</span><span class="sxs-lookup"><span data-stu-id="3e976-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="3e976-107">當 COM + 轉換 **HRESULT** 值時，它會清除所有方法的輸出參數。</span><span class="sxs-lookup"><span data-stu-id="3e976-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="3e976-108">傳回的參考會釋出，並將傳回的物件指標值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3e976-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e976-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e976-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e976-110">錯誤隔離和 Failfast 原則</span><span class="sxs-lookup"><span data-stu-id="3e976-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="3e976-111">找出錯誤的來源</span><span class="sxs-lookup"><span data-stu-id="3e976-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="3e976-112">解讀錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3e976-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="3e976-113">在 COM + 中處理錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="3e976-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="3e976-114">疑難排解</span><span class="sxs-lookup"><span data-stu-id="3e976-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



