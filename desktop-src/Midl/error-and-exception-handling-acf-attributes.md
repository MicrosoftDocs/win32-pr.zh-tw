---
title: 錯誤和例外狀況處理 ACF 屬性
description: 使用下列屬性來處理錯誤。
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL、屬性、錯誤和例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106984515"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="d734b-104">錯誤和例外狀況處理 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="d734b-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="d734b-105">使用下列屬性來處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="d734b-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="d734b-106">屬性</span><span class="sxs-lookup"><span data-stu-id="d734b-106">Attribute</span></span>                                                                | <span data-ttu-id="d734b-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="d734b-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d734b-108">[**通訊 \_ 狀態**](comm-status.md)[**錯誤 \_ 狀態**](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="d734b-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="d734b-109">讓用戶端應用程式以正常方式處理例外狀況，方法是導致通訊和伺服器錯誤以參數值的形式傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="d734b-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="d734b-110">然後，用戶端應用程式可以呼叫 RPC 執行時間函式 [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) ，將錯誤訊息轉送給使用者。</span><span class="sxs-lookup"><span data-stu-id="d734b-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d734b-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d734b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d734b-112">匯入檔案和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="d734b-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 