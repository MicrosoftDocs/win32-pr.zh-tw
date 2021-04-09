---
description: 封裝程式碼是識別特定 Windows Installer 套件的 GUID。
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: 封裝碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115356"
---
# <a name="package-codes"></a><span data-ttu-id="fc034-103">封裝碼</span><span class="sxs-lookup"><span data-stu-id="fc034-103">Package Codes</span></span>

<span data-ttu-id="fc034-104">封裝程式碼是識別特定 Windows Installer [*套件*](p-gly.md)的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fc034-104">The package code is a GUID identifying a particular Windows Installer [*package*](p-gly.md).</span></span> <span data-ttu-id="fc034-105">封裝程式碼會將 .msi 檔案與應用程式或產品產生關聯，也可以用於驗證來源。</span><span class="sxs-lookup"><span data-stu-id="fc034-105">The package code associates an .msi file with an application or product and can also be used for the verification of sources.</span></span> <span data-ttu-id="fc034-106">產品和套件代碼不可互換。</span><span class="sxs-lookup"><span data-stu-id="fc034-106">The product and package codes are not interchangeable.</span></span> <span data-ttu-id="fc034-107">如需詳細資訊，請參閱 [產品代碼](product-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="fc034-107">For details, see [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="fc034-108">Nonidentical .msi 檔案不能有相同的封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="fc034-108">Nonidentical .msi files should not have the same package code.</span></span> <span data-ttu-id="fc034-109">變更封裝程式碼很重要，因為它是安裝程式用來搜尋並驗證指定安裝之正確封裝的主要識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc034-109">It is important to change the package code because it is the primary identifier used by the installer to search for and validate the correct package for a given installation.</span></span> <span data-ttu-id="fc034-110">如果在未變更套件程式碼的情況下變更套件，安裝程式仍可存取安裝程式時，安裝程式可能不會使用較新的套件。</span><span class="sxs-lookup"><span data-stu-id="fc034-110">If a package is changed without changing the package code, the installer may not use the newer package if both are still accessible to the installer.</span></span>

<span data-ttu-id="fc034-111">封裝程式碼會儲存在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="fc034-111">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) Property of the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="fc034-112">請注意，產品代碼和套件程式碼 Guid 中的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="fc034-112">Note that letters in product code and package code GUIDs must be uppercase.</span></span> <span data-ttu-id="fc034-113">GUIDGEN 之類的公用程式會產生包含小寫字母的 Guid。</span><span class="sxs-lookup"><span data-stu-id="fc034-113">Utilities such as GUIDGEN generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="fc034-114">這些 Guid 中的小寫字母必須變更為大寫，才能當做產品代碼或封裝程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="fc034-114">The lowercase letters in these GUIDs must be changed to uppercase to be used as a product code or package code.</span></span>

<span data-ttu-id="fc034-115">雖然傳送具有相同封裝程式碼和產品程式碼的應用程式很常見，但在更新應用程式時，這兩個值可能會分離出來。</span><span class="sxs-lookup"><span data-stu-id="fc034-115">Although it is common to ship an application that has the same package code and product code, the two values can diverge as the application is updated.</span></span> <span data-ttu-id="fc034-116">例如，包含應用程式的新檔案需要更新安裝資料庫以安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="fc034-116">For example, including a new file with the application would require updating the installation database to install the file.</span></span> <span data-ttu-id="fc034-117">如果變更較小，開發人員可能會選擇不變更產品代碼，不過，需要不同的 .msi 檔案才能安裝新的檔案，因此封裝程式碼必須遞增。</span><span class="sxs-lookup"><span data-stu-id="fc034-117">If the changes are minor a developer may choose not to change the product code, however, a different .msi file is needed to install the new file and so the package code must be incremented.</span></span> <span data-ttu-id="fc034-118">相反地，您可以使用單一套件來安裝多項產品。</span><span class="sxs-lookup"><span data-stu-id="fc034-118">Conversely, a single package can be used to install more than one product.</span></span> <span data-ttu-id="fc034-119">例如，在沒有語言轉換的情況下安裝套件，可以安裝英文版的應用程式，而且使用語言轉換安裝相同的套件可能會安裝法文版。</span><span class="sxs-lookup"><span data-stu-id="fc034-119">For example, the installation of a package without a language transform could install the English version of the application and the installation of the same package with a language transform could install the French version.</span></span> <span data-ttu-id="fc034-120">轉換與決定封裝程式碼的 .msi 檔不同。</span><span class="sxs-lookup"><span data-stu-id="fc034-120">The transform is distinct from the .msi file that determines the package code.</span></span> <span data-ttu-id="fc034-121">英文和法文版本可能會有不同的產品代碼和相同的封裝碼，因為兩者都是使用相同的 .msi 檔案來安裝。</span><span class="sxs-lookup"><span data-stu-id="fc034-121">The English and French versions could have different product codes and the same package code because they are both installed with the same .msi file.</span></span>

 

 



