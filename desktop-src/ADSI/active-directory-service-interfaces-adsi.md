---
title: Active Directory 服務介面
description: Active Directory 的服務介面簡介，並連結至不同的指南。
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- 'Active Directory 服務介面 (查看 ADSI) '
- ADSI ADSI、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024091"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="7bcdc-106">Active Directory 服務介面</span><span class="sxs-lookup"><span data-stu-id="7bcdc-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="7bcdc-107">目的</span><span class="sxs-lookup"><span data-stu-id="7bcdc-107">Purpose</span></span>

<span data-ttu-id="7bcdc-108">Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="7bcdc-109">ADSI 用於分散式運算環境中，以呈現一組用於管理網路資源的目錄服務介面。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="7bcdc-110">系統管理員和開發人員可以使用 ADSI 服務來列舉和管理目錄服務中的資源，不論哪一個網路環境包含資源。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="7bcdc-111">ADSI 可啟用一般管理工作，例如新增使用者、管理印表機，以及在分散式運算環境中尋找資源。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="7bcdc-112">下列檔適用于電腦程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="7bcdc-113">如果您是嘗試偵測列印錯誤或家用網路問題的使用者，請參閱 [Microsoft 社區論壇](https://answers.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="7bcdc-114">適用時</span><span class="sxs-lookup"><span data-stu-id="7bcdc-114">Where applicable</span></span>

<span data-ttu-id="7bcdc-115">網路系統管理員可以使用 ADSI 來自動化一般工作，例如新增使用者和群組、管理印表機，以及設定網路資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="7bcdc-116">獨立軟體廠商和使用者開發人員可以使用 ADSI 來「目錄啟用」其產品和應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="7bcdc-117">服務可以在目錄中發佈自己，用戶端可以使用目錄來尋找服務，而且兩者都可以使用目錄來尋找和操作其他感興趣的物件。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="7bcdc-118">由於 Active Directory 服務介面與基礎目錄服務 (的) 無關，因此可支援目錄的產品和應用程式在多個網路和目錄環境中都能順利運作。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7bcdc-119">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="7bcdc-119">Developer audience</span></span>

<span data-ttu-id="7bcdc-120">您可以撰寫許多語言的 ADSI 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="7bcdc-121">針對大部分的系統管理工作，ADSI 定義了可從與 Automation 相容的語言（例如 Microsoft Visual Basic、Microsoft Visual Basic Scripting Edition (VBScript) 和 JAVA）存取的介面和物件，以提供更高效能和效率的語言，例如 C 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="7bcdc-122">在 COM 程式設計中，良好的基礎適用于 ADSI 程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7bcdc-123">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="7bcdc-123">Run-time requirements</span></span>

<span data-ttu-id="7bcdc-124">Active Directory 在 Windows Server 網域控制站上執行。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="7bcdc-125">不過，您可以在 Windows 上撰寫和執行使用 ADSI 的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="7bcdc-126">此外，開發人員也需要平臺軟體發展工具組 (SDK) ，也可在 MSDN 網站上取得。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="7bcdc-127">若要調查 Active Directory 的內容，請使用 Active Directory 消費者和電腦 MMC 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="7bcdc-128">此嵌入式管理單元取代了舊版 Windows 所提供的 Adsvw 工具。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bcdc-129">本節內容</span><span class="sxs-lookup"><span data-stu-id="7bcdc-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7bcdc-130">關於 ADSI</span><span class="sxs-lookup"><span data-stu-id="7bcdc-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="7bcdc-131">ADSI 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="7bcdc-132">使用 ADSI</span><span class="sxs-lookup"><span data-stu-id="7bcdc-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="7bcdc-133">使用 ADSI 的程式設計師指南。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="7bcdc-134">ADSI 快速入門教學課程</span><span class="sxs-lookup"><span data-stu-id="7bcdc-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="7bcdc-135">使用 ADSI 搭配 Automation 來管理目錄。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="7bcdc-136">ADSI 參考</span><span class="sxs-lookup"><span data-stu-id="7bcdc-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="7bcdc-137">ADSI 介面和方法的檔。</span><span class="sxs-lookup"><span data-stu-id="7bcdc-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7bcdc-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bcdc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bcdc-139">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="7bcdc-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="7bcdc-140">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="7bcdc-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="7bcdc-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7bcdc-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 