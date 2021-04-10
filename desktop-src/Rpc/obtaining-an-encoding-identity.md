---
title: 取得編碼身分識別
description: 正在解碼編碼資料的應用程式，可以在呼叫常式將其解碼之前，取得用來將資料編碼的常式識別。 MesInqProcEncodingId 常式會提供此身分識別。
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- 遠端程序呼叫 RPC、工作、取得編碼身分識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674915"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="fef8e-105">取得編碼身分識別</span><span class="sxs-lookup"><span data-stu-id="fef8e-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="fef8e-106">正在解碼編碼資料的應用程式，可以在呼叫常式將其解碼之前，取得用來將資料編碼的常式識別。</span><span class="sxs-lookup"><span data-stu-id="fef8e-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="fef8e-107">[**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid)常式會提供此身分識別。</span><span class="sxs-lookup"><span data-stu-id="fef8e-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="fef8e-108">MIDL 編譯器會為介面中的每個程式指派一個整數識別碼，稱為程式 *識別碼* 或 *proc ID*。</span><span class="sxs-lookup"><span data-stu-id="fef8e-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="fef8e-109">編號開頭為零。</span><span class="sxs-lookup"><span data-stu-id="fef8e-109">Numbering begins with zero.</span></span> <span data-ttu-id="fef8e-110">RPC 執行時間程式庫不涉及將程式識別碼轉譯為實際的程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="fef8e-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="fef8e-111">指定 proc 識別碼之後，您的應用程式必須提供呼叫正確程式的方法。</span><span class="sxs-lookup"><span data-stu-id="fef8e-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="fef8e-112">一般來說，應用程式開發人員會在使用 C/c + + 時，使用一系列的 **if** 語句或 (，) 這個用途的 **switch** 語句。</span><span class="sxs-lookup"><span data-stu-id="fef8e-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




