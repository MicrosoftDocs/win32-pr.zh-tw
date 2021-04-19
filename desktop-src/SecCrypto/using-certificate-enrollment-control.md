---
description: 說明如何建立憑證要求，並在憑證存放區中接收和儲存傳回的憑證。
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: 使用憑證註冊控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac3da319571b164fe66eb5bb3ac647c2978fff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993005"
---
# <a name="using-certificate-enrollment-control"></a><span data-ttu-id="cc7a2-103">使用憑證註冊控制項</span><span class="sxs-lookup"><span data-stu-id="cc7a2-103">Using Certificate Enrollment Control</span></span>

<span data-ttu-id="cc7a2-104">憑證註冊控制項是具有許多屬性和數種方法的單一物件，可用來判斷憑證註冊控制項處理使用者資訊的方式、要要求的憑證類型、產生金鑰的方式、要儲存的憑證，以及相關的進程。</span><span class="sxs-lookup"><span data-stu-id="cc7a2-104">The Certificate Enrollment Control is a single object with many properties and several methods that can be used to determine how the Certificate Enrollment Control processes the user information, the type of certificate to be requested, how the keys are to be generated, where the certificate is to be stored, and related processes.</span></span> <span data-ttu-id="cc7a2-105">憑證註冊控制項有兩種主要用途：建立 (PKCS 10) 的 [*憑證要求*](../secgloss/c-gly.md) \# ，以及接收傳回的憑證並將其儲存在 [*憑證存放區*](../secgloss/c-gly.md)中。</span><span class="sxs-lookup"><span data-stu-id="cc7a2-105">There are two primary uses of the Certificate Enrollment Control: to create a [*certificate request*](../secgloss/c-gly.md) (PKCS \#10), and to receive the returned certificate and store it in a [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="cc7a2-106">如需建立憑證註冊控制項物件的實例、設定其屬性，以及使用其方法的詳細資訊和語法，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="cc7a2-106">For details and syntax for creating an instance of the Certificate Enrollment Control object, setting its properties, and using its methods, see the following topics.</span></span>



| <span data-ttu-id="cc7a2-107">資訊</span><span class="sxs-lookup"><span data-stu-id="cc7a2-107">Information</span></span>                                                                                                                                                                                           | <span data-ttu-id="cc7a2-108">主題</span><span class="sxs-lookup"><span data-stu-id="cc7a2-108">Topic</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7a2-109">以不同的程式設計語言建立憑證註冊控制物件的實例</span><span class="sxs-lookup"><span data-stu-id="cc7a2-109">Creating an instance of the Certificate Enrollment Control object in different programming languages</span></span>                                                                                                  | [<span data-ttu-id="cc7a2-110">建立憑證註冊控制項物件的實例</span><span class="sxs-lookup"><span data-stu-id="cc7a2-110">Creating an Instance of the Certificate Enrollment Control Object</span></span>](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| <span data-ttu-id="cc7a2-111">使用不同程式設計語言的憑證註冊控制項屬性</span><span class="sxs-lookup"><span data-stu-id="cc7a2-111">Using Certificate Enrollment Control properties in different programming languages</span></span>                                                                                                                    | [<span data-ttu-id="cc7a2-112">使用憑證註冊控制項屬性</span><span class="sxs-lookup"><span data-stu-id="cc7a2-112">Using the Certificate Enrollment Control Properties</span></span>](using-the-certificate-enrollment-control-properties.md)                             |
| <span data-ttu-id="cc7a2-113">收集必要的資訊，並以不同的程式設計語言提交 [*憑證要求*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="cc7a2-113">Collecting the necessary information and submitting a [*certificate request*](../secgloss/c-gly.md) in different programming languages.</span></span> | [<span data-ttu-id="cc7a2-114">建立憑證要求</span><span class="sxs-lookup"><span data-stu-id="cc7a2-114">Creating the Certificate Request</span></span>](creating-the-certificate-request.md)                                                                   |
| <span data-ttu-id="cc7a2-115">解壓縮和儲存已完成的憑證</span><span class="sxs-lookup"><span data-stu-id="cc7a2-115">Extracting and storing the completed certificate</span></span>                                                                                                                                                      | [<span data-ttu-id="cc7a2-116">接收傳回的憑證</span><span class="sxs-lookup"><span data-stu-id="cc7a2-116">Receiving the Returned Certificate</span></span>](receiving-the-returned-certificate.md)                                                               |
| <span data-ttu-id="cc7a2-117">從不同語言的傳回值中取出資訊</span><span class="sxs-lookup"><span data-stu-id="cc7a2-117">Retrieving information from return values in different languages</span></span>                                                                                                                                      | [<span data-ttu-id="cc7a2-118">方法傳回值</span><span class="sxs-lookup"><span data-stu-id="cc7a2-118">Method Return Values</span></span>](method-return-values.md)                                                                                           |
| <span data-ttu-id="cc7a2-119">檢查錯誤</span><span class="sxs-lookup"><span data-stu-id="cc7a2-119">Checking for errors</span></span>                                                                                                                                                                                   | [<span data-ttu-id="cc7a2-120">錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="cc7a2-120">Error Checking</span></span>](error-checking.md)                                                                                                       |



 

 

 
