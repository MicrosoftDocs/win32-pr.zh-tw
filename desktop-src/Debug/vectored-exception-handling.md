---
description: 向量化例外狀況處理常式是結構化例外狀況處理的延伸。
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: 向量式例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847295"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="2bc4b-103">向量式例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="2bc4b-103">Vectored Exception Handling</span></span>

<span data-ttu-id="2bc4b-104">向量化例外狀況處理常式是結構化例外狀況處理的延伸。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="2bc4b-105">應用程式可以註冊函式，以監看或處理應用程式的所有例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="2bc4b-106">向量處理常式不是以框架為基礎，因此您可以加入將呼叫的處理常式，而不論您在呼叫框架中的哪個位置。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="2bc4b-107">向量處理常式會依其加入的順序來呼叫，偵錯工具會取得第一次可能的通知，但在系統開始回溯堆疊之前。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="2bc4b-108">若要加入向量 continue 處理常式，請使用 [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) 函數。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="2bc4b-109">若要移除這個處理常式，請使用 [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) 函數。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="2bc4b-110">若要加入向量式例外狀況處理常式，請使用 [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) 函數。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="2bc4b-111">若要移除這個處理常式，請使用 [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) 函數。</span><span class="sxs-lookup"><span data-stu-id="2bc4b-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
