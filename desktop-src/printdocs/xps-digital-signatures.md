---
description: XPS 數位簽章 API 可讓使用者簽署檔、確認簽署者的身分識別，並指出 XPS 檔在簽署之後是否已經變更。
ms.assetid: 8a23617e-92fe-4662-b602-47add5716358
title: XPS 數位簽章 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c56485a532afbb148e62901c38db49ab81963c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997190"
---
# <a name="xps-digital-signature-api"></a><span data-ttu-id="0b3bb-103">XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="0b3bb-103">XPS Digital Signature API</span></span>

<span data-ttu-id="0b3bb-104">XPS 數位簽章 API 可讓使用者簽署檔、確認簽署者的身分識別，並指出 XPS 檔在簽署之後是否已經變更。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-104">The XPS Digital Signature API enables a user to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="0b3bb-105">XPS 數位簽章 API 建基於開放式封裝慣例中使用的數位簽章技術，這項技術是在 [標準 ECMA-376、Office OPEN XML 檔案格式](https://www.ecma-international.org/publications/standards/Ecma-376.htm)的第1版、第2部分「開放式封裝慣例」中指定。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-105">The XPS Digital Signature API is built on the digital signature technology that is used in the Open Packaging Conventions, which are specified in the 1st edition, Part 2, "Open Packaging Conventions," of [Standard ECMA-376, Office Open XML File Formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0b3bb-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="0b3bb-106">In This Section</span></span>

<span data-ttu-id="0b3bb-107">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-107">This section contains the following topics.</span></span>

### <a name="about-xps-digital-signature-api"></a><span data-ttu-id="0b3bb-108">關於 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="0b3bb-108">About XPS Digital Signature API</span></span>

<span data-ttu-id="0b3bb-109">[關於 Xps 數位簽章 api](about-xps-digital-signatures.md) ，請以高階的說明 Xps 數位簽章 api。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-109">[About XPS Digital Signature API](about-xps-digital-signatures.md) describes the XPS Digital Signature API at a high level.</span></span>

### <a name="using-xps-digital-signature-api"></a><span data-ttu-id="0b3bb-110">使用 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="0b3bb-110">Using XPS Digital Signature API</span></span>

<span data-ttu-id="0b3bb-111">[使用 Xps 數位簽章 api](using-digital-signatures-in-xps-documents.md) 說明如何使用 Xps 數位簽章 api。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-111">[Using XPS Digital Signature API](using-digital-signatures-in-xps-documents.md) describes how to use the XPS Digital Signature API.</span></span>

### <a name="xps-digital-signatures-reference"></a><span data-ttu-id="0b3bb-112">XPS 數位簽章參考</span><span class="sxs-lookup"><span data-stu-id="0b3bb-112">XPS Digital Signatures Reference</span></span>

<span data-ttu-id="0b3bb-113">[Xps 數位簽章 Api 參考](xps-digital-signatures-programming-reference.md)包含由 Xps 數位簽章 api 所執行之介面、方法和枚舉器的完整清單。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-113">The [XPS Digital Signature API Reference](xps-digital-signatures-programming-reference.md) contains a complete listing of the interfaces, methods, and enumerators that are implemented by the XPS Digital Signatures API.</span></span>

## <a name="platform-update-for-windows-vista"></a><span data-ttu-id="0b3bb-114">Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="0b3bb-114">Platform Update for Windows Vista</span></span>

<span data-ttu-id="0b3bb-115">Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新不支援本節所述的 XPS 數位簽章介面。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-115">The XPS Digital Signature interfaces that are described in this section are not supported by the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="0b3bb-116">需要這些介面的應用程式應該在 Windows 7 或更新版本上執行，或是在 Windows Server 2008 R2 或更新版本上執行。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-116">An application that requires these interfaces should run on Windows 7 or later, or on Windows Server 2008 R2 or later.</span></span> <span data-ttu-id="0b3bb-117">否則，應用程式可能不會為使用者提供應用程式的完整功能。</span><span class="sxs-lookup"><span data-stu-id="0b3bb-117">Otherwise, the application may not provide the user with the application's complete functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b3bb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b3bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b3bb-119">包裝</span><span class="sxs-lookup"><span data-stu-id="0b3bb-119">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="0b3bb-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="0b3bb-120">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="0b3bb-121">標準 ECMA-376、Office Open XML 檔案格式</span><span class="sxs-lookup"><span data-stu-id="0b3bb-121">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
