---
description: 完成作業可讓應用程式指定當忙碌目的地之類的因素無法正常連接時，如何處理會話。
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: 完成會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971047"
---
# <a name="complete-a-session"></a><span data-ttu-id="ab728-103">完成會話</span><span class="sxs-lookup"><span data-stu-id="ab728-103">Complete a Session</span></span>

<span data-ttu-id="ab728-104">完成作業可讓應用程式指定當忙碌目的地之類的因素無法正常連接時，如何處理會話。</span><span class="sxs-lookup"><span data-stu-id="ab728-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="ab728-105">[LINECALLCOMPLMODE \_ 常數](./linecallcomplmode--constants.md)會根據服務提供者的功能，定義應用程式可能會有的可能選項。</span><span class="sxs-lookup"><span data-stu-id="ab728-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="ab728-106">指定位址的多個呼叫完成要求可能在任何一次都未完成。</span><span class="sxs-lookup"><span data-stu-id="ab728-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="ab728-107">為了識別個別的要求，此實作為會傳回 [完成識別碼](completion-id-ovr.md)。</span><span class="sxs-lookup"><span data-stu-id="ab728-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="ab728-108">取消通話完成要求正在進行中，也會使用此呼叫完成識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab728-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="ab728-109">**TAPI 2.x：** 請參閱 [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall)、 [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall)。</span><span class="sxs-lookup"><span data-stu-id="ab728-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="ab728-110">**TAPI 3.x：** 請參閱 [**ITBasicCallControl：： Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)、 [**ITBasicCallControl：:D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)。</span><span class="sxs-lookup"><span data-stu-id="ab728-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
