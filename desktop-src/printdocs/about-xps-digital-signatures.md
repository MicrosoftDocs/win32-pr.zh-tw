---
description: 本節提供 XPS 數位簽章 API 的總覽。
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: 關於 XPS 數位簽章 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115485"
---
# <a name="about-xps-digital-signature-api"></a><span data-ttu-id="daf73-103">關於 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="daf73-103">About XPS Digital Signature API</span></span>

<span data-ttu-id="daf73-104">XPS 檔可以有數位簽章，讓使用者可以簽署檔、確認簽署者的身分識別，並指出 XPS 檔在簽署之後是否已經變更。</span><span class="sxs-lookup"><span data-stu-id="daf73-104">XPS documents can have digital signatures to allow users to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="daf73-105">原生 Windows 應用程式可以使用 XPS 數位簽章 API 的介面來執行 XPS 檔的數位簽章作業。</span><span class="sxs-lookup"><span data-stu-id="daf73-105">A native Windows application can use the interfaces of the XPS Digital Signature API to perform digital signature operations on an XPS document.</span></span> <span data-ttu-id="daf73-106">本節提供 XPS 數位簽章 API 的總覽。</span><span class="sxs-lookup"><span data-stu-id="daf73-106">This section provides an overview of the XPS Digital Signature API.</span></span>

<span data-ttu-id="daf73-107">[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)介面會管理 XPS 檔的數位簽章作業。</span><span class="sxs-lookup"><span data-stu-id="daf73-107">The [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface manages the digital signature operations on an XPS document.</span></span> <span data-ttu-id="daf73-108">應用程式必須先呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 **IXpsSignatureManager** ，然後呼叫 [**IXpsSignatureManager：： LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) 或 [**IXpsSignatureManager：： LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) 來載入 xps 檔，應用程式才能存取 xps 檔的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="daf73-108">Before an application can access the digital signatures of an XPS document, the application must call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an **IXpsSignatureManager** and then call [**IXpsSignatureManager::LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**IXpsSignatureManager::LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) to load the XPS document.</span></span> <span data-ttu-id="daf73-109">如需此初始化程式的詳細資訊，請參閱初始化簽章 [管理員](initialize-the-signature-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="daf73-109">For more information about this initialization process, see [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="daf73-110">將 XPS 檔載入 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) 介面之後，應用程式就可以存取檔的數位簽章和數位簽章要求。</span><span class="sxs-lookup"><span data-stu-id="daf73-110">After an XPS document has been loaded into an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface, an application can then access the document's digital signatures and digital signature requests.</span></span> <span data-ttu-id="daf73-111">您可以使用簽章管理員的 [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)介面中的 [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)介面來存取數位簽章。</span><span class="sxs-lookup"><span data-stu-id="daf73-111">You can access the digital signatures by using an [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface from the signature manager's [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) interface.</span></span> <span data-ttu-id="daf73-112">應用程式也可以新增和移除集合中的 **IXpsSignature** 介面。</span><span class="sxs-lookup"><span data-stu-id="daf73-112">An application can also add and remove **IXpsSignature** interfaces from the collection.</span></span> <span data-ttu-id="daf73-113">您可以使用在 [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)介面中收集的 [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)來存取簽章要求。</span><span class="sxs-lookup"><span data-stu-id="daf73-113">Signature requests are accessed by using [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) which are collected in an [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) interface.</span></span> <span data-ttu-id="daf73-114">**IXpsSignatureRequestCollection** 是 [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)介面的一部分，會在簽章管理員的 [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)中收集。</span><span class="sxs-lookup"><span data-stu-id="daf73-114">The **IXpsSignatureRequestCollection** is part of an [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interface which are collected in the [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) of the signature manager.</span></span>

<span data-ttu-id="daf73-115">應用程式可以使用簽章管理員的 [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) 來存取和設定數位簽章選項。</span><span class="sxs-lookup"><span data-stu-id="daf73-115">Applications can use the [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) of the signature manager to access and set digital signature options.</span></span>

<span data-ttu-id="daf73-116">如需如何存取 XPS 檔數位簽章的範例，請參閱常見的 [數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作。</span><span class="sxs-lookup"><span data-stu-id="daf73-116">For examples of how to access the digital signatures of an XPS document, see [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="daf73-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="daf73-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf73-118">使用 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="daf73-118">Using XPS Digital Signature API</span></span>](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[<span data-ttu-id="daf73-119">XPS 數位簽章 API 參考</span><span class="sxs-lookup"><span data-stu-id="daf73-119">XPS Digital Signature API Reference</span></span>](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="daf73-120">包裝</span><span class="sxs-lookup"><span data-stu-id="daf73-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="daf73-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="daf73-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="daf73-122">標準 ECMA-376、Office Open XML 檔案格式</span><span class="sxs-lookup"><span data-stu-id="daf73-122">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
