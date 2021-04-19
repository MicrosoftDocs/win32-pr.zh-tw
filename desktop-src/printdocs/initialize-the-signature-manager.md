---
description: 本主題說明如何初始化簽章管理員以搭配 XPS 檔使用。
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: 初始化簽章管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984734"
---
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="2bf0c-103">初始化簽章管理員</span><span class="sxs-lookup"><span data-stu-id="2bf0c-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="2bf0c-104">本主題說明如何初始化簽章管理員以搭配 XPS 檔使用。</span><span class="sxs-lookup"><span data-stu-id="2bf0c-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="2bf0c-105">在您的程式中使用下列程式碼範例之前，請閱讀 [一般數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="2bf0c-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="2bf0c-106">若要使用密碼編譯 API 的 Windows 7 功能，請定義 **CRYPT \_ OID \_ 資訊 \_ 具有 \_ 額外的 \_ 欄位** 符號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2bf0c-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="2bf0c-107">接下來，呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)以具現化 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)介面，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="2bf0c-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



<span data-ttu-id="2bf0c-108">[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)具現化的介面只能由一個 XPS 檔使用，必須先呼叫 [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile)或 [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream)載入，然後再呼叫任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="2bf0c-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="2bf0c-109">在具現化 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) 介面並載入 XPS 檔之後，簽章管理員便已可供使用。</span><span class="sxs-lookup"><span data-stu-id="2bf0c-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bf0c-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bf0c-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2bf0c-111">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="2bf0c-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="2bf0c-112">簽署檔</span><span class="sxs-lookup"><span data-stu-id="2bf0c-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="2bf0c-113">將簽名要求新增至 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="2bf0c-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="2bf0c-114">驗證檔簽章</span><span class="sxs-lookup"><span data-stu-id="2bf0c-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="2bf0c-115">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="2bf0c-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="2bf0c-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="2bf0c-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="2bf0c-117">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="2bf0c-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="2bf0c-118">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="2bf0c-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="2bf0c-119">XPS 數位簽章 API 錯誤</span><span class="sxs-lookup"><span data-stu-id="2bf0c-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="2bf0c-120">XPS 檔錯誤</span><span class="sxs-lookup"><span data-stu-id="2bf0c-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="2bf0c-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="2bf0c-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
