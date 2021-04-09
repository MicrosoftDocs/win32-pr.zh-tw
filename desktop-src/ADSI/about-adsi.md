---
title: 關於 Active Directory 服務介面
description: " (ADSI) 的 Active Directory 服務介面，會將目錄服務的功能從分散式運算環境中的不同網路提供者抽象化，以提供一組用來管理網路資源的目錄服務介面。"
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- 關於 Active Directory 服務介面 ADSI
- ADSI ADSI，關於
- Active Directory 服務介面 ADSI，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092205"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="edccc-106">關於 Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="edccc-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="edccc-107"> (ADSI) 的 Active Directory 服務介面，會將目錄服務的功能從分散式運算環境中的不同網路提供者抽象化，以提供一組用來管理網路資源的目錄服務介面。</span><span class="sxs-lookup"><span data-stu-id="edccc-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="edccc-108">系統管理員和開發人員可以使用 ADSI 服務來列舉和管理目錄服務中的資源，不論哪一個網路環境包含資源。</span><span class="sxs-lookup"><span data-stu-id="edccc-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="edccc-109">ADSI 可讓您更輕鬆地執行一般管理工作，例如新增使用者、管理印表機，以及尋找整個分散式運算環境中的資源。</span><span class="sxs-lookup"><span data-stu-id="edccc-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="edccc-110">ADSI 讓開發人員可以輕鬆地「目錄啟用」應用程式。</span><span class="sxs-lookup"><span data-stu-id="edccc-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="edccc-111">無論安裝哪一種目錄服務，系統管理員和開發人員都會處理一組目錄服務介面。</span><span class="sxs-lookup"><span data-stu-id="edccc-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="edccc-112">本簡介將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="edccc-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="edccc-113">多個目錄服務</span><span class="sxs-lookup"><span data-stu-id="edccc-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="edccc-114">誰將使用 Active Directory 服務介面？</span><span class="sxs-lookup"><span data-stu-id="edccc-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="edccc-115">今天的目錄服務</span><span class="sxs-lookup"><span data-stu-id="edccc-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="edccc-116">使用 Active Directory 服務介面的優點</span><span class="sxs-lookup"><span data-stu-id="edccc-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="edccc-117">Active Directory 服務介面架構</span><span class="sxs-lookup"><span data-stu-id="edccc-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="edccc-118">程式設計語言支援</span><span class="sxs-lookup"><span data-stu-id="edccc-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="edccc-119">ADSI 屬性和屬性</span><span class="sxs-lookup"><span data-stu-id="edccc-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="edccc-120">閱讀本指南之前，您應該知道的事項</span><span class="sxs-lookup"><span data-stu-id="edccc-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="edccc-121">本指南假設您熟悉元件物件模型 (COM) 和自動化，而且您知道如何在 Visual Basic 或 C/c + + 中進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="edccc-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="edccc-122">本指南中使用的某些詞彙對 ADSI 或目錄服務環境而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="edccc-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="edccc-123">其他詞彙會很熟悉，但在這些環境中可能會有稍微不同的意義。</span><span class="sxs-lookup"><span data-stu-id="edccc-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="edccc-124">進一步閱讀 ADSI 和相關主題</span><span class="sxs-lookup"><span data-stu-id="edccc-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="edccc-125">如需 Active Directory 服務介面及其基礎技術的詳細資訊，您可能會發現下列來源有説明。</span><span class="sxs-lookup"><span data-stu-id="edccc-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="edccc-126">Brockschmidt、Kraig。</span><span class="sxs-lookup"><span data-stu-id="edccc-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="edccc-127">*在 OLE*、第2版內。</span><span class="sxs-lookup"><span data-stu-id="edccc-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="edccc-128">華盛頓州 Redmond，WA： Microsoft 按下，1995。</span><span class="sxs-lookup"><span data-stu-id="edccc-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="edccc-129">Chappell，David。</span><span class="sxs-lookup"><span data-stu-id="edccc-129">Chappell, David.</span></span> <span data-ttu-id="edccc-130">*瞭解 ActiveX 和 OLE*。</span><span class="sxs-lookup"><span data-stu-id="edccc-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="edccc-131">華盛頓州 Redmond，WA： Microsoft 按下，1996。</span><span class="sxs-lookup"><span data-stu-id="edccc-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="edccc-132">Hahn、Steven。</span><span class="sxs-lookup"><span data-stu-id="edccc-132">Hahn, Steven.</span></span> <span data-ttu-id="edccc-133">*ADSI ASP 程式設計人員參考*。</span><span class="sxs-lookup"><span data-stu-id="edccc-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="edccc-134">Wrox，請按1998。</span><span class="sxs-lookup"><span data-stu-id="edccc-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="edccc-135">Harrison、Richard。</span><span class="sxs-lookup"><span data-stu-id="edccc-135">Harrison, Richard.</span></span> <span data-ttu-id="edccc-136">*ASP/MTS/ADSI Web 安全性*。</span><span class="sxs-lookup"><span data-stu-id="edccc-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="edccc-137">Prentice 廳，1999。</span><span class="sxs-lookup"><span data-stu-id="edccc-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="edccc-138">Microsoft OLE DB 程式設計人員參考1.0、1996版。</span><span class="sxs-lookup"><span data-stu-id="edccc-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="edccc-139">*OLE 2 程式設計人員參考，第二* 部。</span><span class="sxs-lookup"><span data-stu-id="edccc-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="edccc-140">華盛頓州 Redmond，WA： Microsoft 按下，1994。</span><span class="sxs-lookup"><span data-stu-id="edccc-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="edccc-141">Rogerson、Dale。</span><span class="sxs-lookup"><span data-stu-id="edccc-141">Rogerson, Dale.</span></span> <span data-ttu-id="edccc-142">*在 COM 內*。</span><span class="sxs-lookup"><span data-stu-id="edccc-142">*Inside COM*.</span></span> <span data-ttu-id="edccc-143">華盛頓州 Redmond，WA： Microsoft 按下，1997。</span><span class="sxs-lookup"><span data-stu-id="edccc-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="edccc-144">*Active Directory 服務設計規格2.0 版*。</span><span class="sxs-lookup"><span data-stu-id="edccc-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="edccc-145">*元件物件模型規格*。</span><span class="sxs-lookup"><span data-stu-id="edccc-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="edccc-146"> (這些資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="edccc-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




