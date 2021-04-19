---
description: 下列介面可以用來註冊憑證階層中的使用者或電腦。
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: 憑證註冊介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994563"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="e6dd4-103">憑證註冊介面</span><span class="sxs-lookup"><span data-stu-id="e6dd4-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="e6dd4-104">下列介面可以用來註冊憑證階層中的使用者或電腦。</span><span class="sxs-lookup"><span data-stu-id="e6dd4-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="e6dd4-105">介面</span><span class="sxs-lookup"><span data-stu-id="e6dd4-105">Interface</span></span>                                              | <span data-ttu-id="e6dd4-106">描述</span><span class="sxs-lookup"><span data-stu-id="e6dd4-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6dd4-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="e6dd4-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="e6dd4-108">註冊憑證階層中的電腦或使用者。</span><span class="sxs-lookup"><span data-stu-id="e6dd4-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="e6dd4-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="e6dd4-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="e6dd4-110">擴充 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 介面，以從範本啟用初始化。</span><span class="sxs-lookup"><span data-stu-id="e6dd4-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="e6dd4-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="e6dd4-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="e6dd4-112">定義可讓 web 應用程式註冊憑證、將原則伺服器認證儲存在認證快取中，以及註冊原則伺服器和註冊伺服器的方法。</span><span class="sxs-lookup"><span data-stu-id="e6dd4-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="e6dd4-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="e6dd4-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="e6dd4-114">捕獲憑證註冊交易的詳細錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="e6dd4-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="e6dd4-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="e6dd4-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="e6dd4-116">X.509 Simple Computer 註冊 Protocol 介面</span><span class="sxs-lookup"><span data-stu-id="e6dd4-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="e6dd4-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6dd4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6dd4-118">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="e6dd4-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




