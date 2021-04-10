---
description: 每個憑證註冊控制項屬性都是讀取/寫入，而且具有初始化的預設值以及一組可接受的值。
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: 使用憑證註冊控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691395"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="0953b-103">使用憑證註冊控制項屬性</span><span class="sxs-lookup"><span data-stu-id="0953b-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="0953b-104">每個憑證註冊控制項屬性都是讀取/寫入，而且具有初始化的預設值以及一組可接受的值。</span><span class="sxs-lookup"><span data-stu-id="0953b-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="0953b-105">您可以將屬性設定為此集合中的任何值，以修改使用屬性之方法的行為。</span><span class="sxs-lookup"><span data-stu-id="0953b-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="0953b-106">若要取得所需的行為，請先設定屬性，然後再呼叫使用該屬性值的方法。</span><span class="sxs-lookup"><span data-stu-id="0953b-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="0953b-107">不過請注意，在呼叫下列方法之後</span><span class="sxs-lookup"><span data-stu-id="0953b-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="0953b-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="0953b-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="0953b-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="0953b-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="0953b-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="0953b-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="0953b-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="0953b-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="0953b-112">下列屬性已封鎖而無法重設</span><span class="sxs-lookup"><span data-stu-id="0953b-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="0953b-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="0953b-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="0953b-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="0953b-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="0953b-115">**ProviderFlags**</span><span class="sxs-lookup"><span data-stu-id="0953b-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="0953b-116">**容器**</span><span class="sxs-lookup"><span data-stu-id="0953b-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="0953b-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="0953b-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="0953b-118">除非呼叫 [**ICEnroll4：： Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) 方法。</span><span class="sxs-lookup"><span data-stu-id="0953b-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="0953b-119">如需個別屬性和方法的詳細資訊，請參閱 [密碼編譯參考](cryptography-reference.md)中這些屬性和方法的參考主題。</span><span class="sxs-lookup"><span data-stu-id="0953b-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="0953b-120">下列各節包含設定和取得憑證註冊控制項屬性的特定語言資訊：</span><span class="sxs-lookup"><span data-stu-id="0953b-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="0953b-121">C + + 中的憑證註冊控制項屬性</span><span class="sxs-lookup"><span data-stu-id="0953b-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
