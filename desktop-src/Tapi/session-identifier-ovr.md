---
description: TAPI 指派每個會話和應用程式都是唯一的會話識別碼。
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: 工作階段識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386296"
---
# <a name="session-identifier"></a><span data-ttu-id="f6a63-103">工作階段識別碼</span><span class="sxs-lookup"><span data-stu-id="f6a63-103">Session Identifier</span></span>

<span data-ttu-id="f6a63-104">TAPI 指派每個會話和應用程式都是唯一的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a63-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="f6a63-105">應用程式會使用會話識別碼與特定會話相關的 TAPI 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f6a63-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="f6a63-106">應用程式通常會藉由建立新的通訊會話或 TAPI 提供會話，來取得識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a63-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="f6a63-107">會話識別碼無法用來將資訊傳遞給另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="f6a63-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="f6a63-108">基於此目的，請使用服務提供者可能指派的 [呼叫識別碼](call-id-ovr.md)。</span><span class="sxs-lookup"><span data-stu-id="f6a63-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="f6a63-109">如需建立會話並傳回會話識別碼之作業的相關資訊，請參閱 [起始會話](initiate-a-session-ovr.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6a63-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="f6a63-110">如需從 TAPI 取得會話識別碼的作業，請參閱 [回應從其他位置起始的會話](respond-to-session-initiated-elsewhere-ovr.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6a63-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="f6a63-111">如需釋放會話資源的詳細資訊，請參閱 [終止會話](terminate-a-session-ovr.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6a63-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="f6a63-112">所有服務提供者都必須支援某種形式的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a63-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="f6a63-113">**TAPI 2.x：** 通訊會話的主要識別碼是呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="f6a63-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="f6a63-114">**TAPI 3.x：** 會話是由 [呼叫物件](call-object.md) 表示，而主要識別碼是指向 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f6a63-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



