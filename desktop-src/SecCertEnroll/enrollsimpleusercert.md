---
description: 使用範本、主體名稱和金鑰長度（以位為單位），向憑證授權單位單位註冊 (CA) 的終端使用者。
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026974"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="600ac-103">enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="600ac-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="600ac-104">EnrollSimpleUserCert 範例會使用範本、主體名稱和金鑰長度（以位為單位），向使用者註冊憑證授權單位單位 (CA) 。</span><span class="sxs-lookup"><span data-stu-id="600ac-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="600ac-105">Location</span><span class="sxs-lookup"><span data-stu-id="600ac-105">Location</span></span>

<span data-ttu-id="600ac-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，根據預設，系統會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ enrollSimpleUserCert 資料夾中安裝 c + + 版本的範例。</span><span class="sxs-lookup"><span data-stu-id="600ac-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="600ac-107">C # 版本安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ X509 憑證註冊 \\ CSharp \\ EnrollSimpleUserCert 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="600ac-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="600ac-108">討論</span><span class="sxs-lookup"><span data-stu-id="600ac-108">Discussion</span></span>

<span data-ttu-id="600ac-109">EnrollSimpleUserCert 範例：</span><span class="sxs-lookup"><span data-stu-id="600ac-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="600ac-110">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="600ac-110">Processes the command line arguments.</span></span> <span data-ttu-id="600ac-111">命令列應該包含範本的名稱、主體名稱和金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="600ac-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="600ac-112">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用範本將它初始化。</span><span class="sxs-lookup"><span data-stu-id="600ac-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="600ac-113">從註冊物件中抓取內部憑證要求物件，並針對 [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) 物件進行查詢。</span><span class="sxs-lookup"><span data-stu-id="600ac-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="600ac-114">最內層的要求一律是 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="600ac-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="600ac-115">從 PKCS 10 要求抓取 [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) 物件 \# ，並設定命令列上指定的金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="600ac-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="600ac-116">建立 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件，並使用它來編碼 X. 500 主體名稱，並將名稱新增至 PKCS \# 10 要求。</span><span class="sxs-lookup"><span data-stu-id="600ac-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="600ac-117">嘗試向 CA 註冊終端使用者，並監視註冊程式的進度。</span><span class="sxs-lookup"><span data-stu-id="600ac-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="600ac-118">CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="600ac-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="600ac-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="600ac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600ac-120">PKCS \# 10 要求</span><span class="sxs-lookup"><span data-stu-id="600ac-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="600ac-121">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="600ac-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



