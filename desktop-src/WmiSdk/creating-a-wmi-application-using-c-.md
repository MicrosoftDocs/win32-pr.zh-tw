---
description: 若要使用 c + + 建立適用于 WMI 的應用程式：您必須初始化 COM、存取和設定 WMI 通訊協定，以及執行手動清除。
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: 使用 c + + 建立 WMI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320339"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="93499-103">使用 c + + 建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="93499-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="93499-104">若要使用 c + + 建立適用于 WMI 的應用程式：您必須初始化 COM、存取和設定 WMI 通訊協定，以及執行手動清除。</span><span class="sxs-lookup"><span data-stu-id="93499-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="93499-105">不過，c + + 的確具有彈性和威力的優點。</span><span class="sxs-lookup"><span data-stu-id="93499-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="93499-106">因此，當您在使用 Visual Basic Scripting Edition (VBScript) 或 Windows PowerShell 處理簡單的程式時，c + + 適用于更複雜的應用程式，而且是撰寫 [提供者](providing-data-to-wmi.md)的必要項。</span><span class="sxs-lookup"><span data-stu-id="93499-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="93499-107">下列程式說明如何建立 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="93499-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="93499-108">**建立 WMI 應用程式**</span><span class="sxs-lookup"><span data-stu-id="93499-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="93499-109">[初始化 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="93499-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="93499-110">由於 WMI 是以 COM 技術為基礎，因此您必須對 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數進行呼叫，才能存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="93499-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="93499-111">[建立連至 WMI 命名空間的](creating-a-connection-to-a-wmi-namespace.md)連線。</span><span class="sxs-lookup"><span data-stu-id="93499-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="93499-112">根據定義，WMI 會在與您的應用程式不同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="93499-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="93499-113">因此，您必須建立應用程式與 WMI 之間的連接。</span><span class="sxs-lookup"><span data-stu-id="93499-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="93499-114">[設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="93499-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="93499-115">若要使用您建立至 WMI 的連接，您必須設定應用程式的模擬和驗證層級。</span><span class="sxs-lookup"><span data-stu-id="93499-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="93499-116">執行應用程式的用途。</span><span class="sxs-lookup"><span data-stu-id="93499-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="93499-117">WMI 公開各種 COM 介面，用來存取和管理整個企業的資料。</span><span class="sxs-lookup"><span data-stu-id="93499-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="93499-118">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [接收 wmi 事件](receiving-a-wmi-event.md)，以及 [適用于 wmi 的 COM API](com-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="93499-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="93499-119">這是您的 WMI 用戶端應用程式的大部分應該存在的位置，例如存取 WMI 物件或運算元據。</span><span class="sxs-lookup"><span data-stu-id="93499-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="93499-120">[清除和關閉您的應用程式](cleaning-up-and-shutting-down-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="93499-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="93499-121">完成對 WMI 的查詢之後，您應該終結所有的 COM 指標，並正確地關閉您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="93499-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="93499-122">如需有關如何建立 WMI 應用程式的詳細資訊和程式碼範例，請參閱 [範例：建立 Wmi 應用程式](example-creating-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="93499-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
