---
description: 從個人資訊交換將已註冊的憑證 (PFX) 檔案安裝至憑證存放區。
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944959"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="17869-103">installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="17869-103">installResponseFromPFX</span></span>

<span data-ttu-id="17869-104">InstallResponseFromPFX 範例會將個人資訊交換 (PFX) 檔案中的已註冊憑證安裝至憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="17869-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="17869-105">Location</span><span class="sxs-lookup"><span data-stu-id="17869-105">Location</span></span>

<span data-ttu-id="17869-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，此範例預設會安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ installResponseFromPFX 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="17869-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="17869-107">討論</span><span class="sxs-lookup"><span data-stu-id="17869-107">Discussion</span></span>

<span data-ttu-id="17869-108">InstallResponseFromPFX 範例：</span><span class="sxs-lookup"><span data-stu-id="17869-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="17869-109">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="17869-109">Processes the command line arguments.</span></span> <span data-ttu-id="17869-110">命令列應該包含：</span><span class="sxs-lookup"><span data-stu-id="17869-110">The command line should contain:</span></span>
    -   <span data-ttu-id="17869-111">範例的名稱。</span><span class="sxs-lookup"><span data-stu-id="17869-111">The name of the sample.</span></span>
    -   <span data-ttu-id="17869-112">包含已註冊憑證之 PFX 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="17869-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="17869-113">與 PFX 檔案相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="17869-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="17869-114">讀取 PFX 檔案，如果 base64 失敗，則先嘗試 base64 格式，以及二進位格式。</span><span class="sxs-lookup"><span data-stu-id="17869-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="17869-115">DecodeFileW () 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="17869-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="17869-116">將已註冊的憑證轉換成 **BSTR** ，並用它來初始化 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件。</span><span class="sxs-lookup"><span data-stu-id="17869-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="17869-117">ConvertWszToBstr 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="17869-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="17869-118">將憑證安裝在憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="17869-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17869-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="17869-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17869-120">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="17869-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="17869-121">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="17869-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



