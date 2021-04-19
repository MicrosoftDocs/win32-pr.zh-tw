---
description: 使用 Certmgr.msc 從檔案或憑證存放區中查看憑證、Crl 和 Ctl、將憑證複製到憑證存放區、從憑證存放區刪除憑證，以及將憑證儲存至檔案。
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: 使用 Certmgr.msc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974553"
---
# <a name="using-certmgr"></a><span data-ttu-id="4bec9-103">使用 Certmgr.msc</span><span class="sxs-lookup"><span data-stu-id="4bec9-103">Using CertMgr</span></span>

<span data-ttu-id="4bec9-104">[Certmgr.msc](certmgr.md) 可以用來查看 [*憑證*](../secgloss/c-gly.md)、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 和 [*憑證信任清單*](../secgloss/c-gly.md) (ctl) 自檔案或憑證存放區、將憑證複製到 [*證書*](../secgloss/c-gly.md)存儲、從憑證存放區刪除憑證，以及將憑證儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="4bec9-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="4bec9-105">當使用 [certmgr.msc](certmgr.md) 時沒有選項時，會出現 certmgr.msc wizard 來引導使用者完成此操作。</span><span class="sxs-lookup"><span data-stu-id="4bec9-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="4bec9-106">檔案必須是下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="4bec9-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="4bec9-107">編碼的 CTL、CRL 或憑證檔案 (可以是以64為基礎的編碼) </span><span class="sxs-lookup"><span data-stu-id="4bec9-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="4bec9-108">PKCS \# 7 檔案</span><span class="sxs-lookup"><span data-stu-id="4bec9-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="4bec9-109">SPC 檔案</span><span class="sxs-lookup"><span data-stu-id="4bec9-109">An SPC file</span></span>
-   <span data-ttu-id="4bec9-110">簽署的檔</span><span class="sxs-lookup"><span data-stu-id="4bec9-110">A signed document</span></span>
-   <span data-ttu-id="4bec9-111">序列化的 storeFile</span><span class="sxs-lookup"><span data-stu-id="4bec9-111">A serialized storeFile</span></span>

<span data-ttu-id="4bec9-112">下列範例會使用 [certmgr.msc](certmgr.md) 命令來執行一般的憑證工作。</span><span class="sxs-lookup"><span data-stu-id="4bec9-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="4bec9-113">從 *myfile.txt* 查看憑證、Crl 和 ctl。</span><span class="sxs-lookup"><span data-stu-id="4bec9-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="4bec9-114">**Certmgr.msc** *myfile.txt ext*</span><span class="sxs-lookup"><span data-stu-id="4bec9-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="4bec9-115">從 [我的系統] 存放區查看憑證、Crl 和 Ctl。</span><span class="sxs-lookup"><span data-stu-id="4bec9-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="4bec9-116">**certmgr.msc-s**</span><span class="sxs-lookup"><span data-stu-id="4bec9-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="4bec9-117">將名為 *myfile.txt* 的檔案中的所有憑證、Crl 和 ctl 複製到稱為 *NewFile* 的新檔案中。</span><span class="sxs-lookup"><span data-stu-id="4bec9-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="4bec9-118">**certmgr.msc-add-all-c** *myfile.txt.* *ext*</span><span class="sxs-lookup"><span data-stu-id="4bec9-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="4bec9-119">將 [我的系統] 存放區中的所有憑證、Crl 和 Ctl 複製到名為 *NewMyFile* 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4bec9-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="4bec9-120">**certmgr.msc-add-all-c-s my** *NewMyFile ext*</span><span class="sxs-lookup"><span data-stu-id="4bec9-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="4bec9-121">將 [我的系統] 存放區中的一般名稱 *mycert.cer* 的憑證複製到名為 *NewCert* 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4bec9-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="4bec9-122">**certmgr.msc-add-c-n** *mycert.cer* **-s my** *NewCert .cer*</span><span class="sxs-lookup"><span data-stu-id="4bec9-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="4bec9-123">刪除 [我的系統] 存放區中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="4bec9-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="4bec9-124">**certmgr.msc-del-全部-c-s**</span><span class="sxs-lookup"><span data-stu-id="4bec9-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="4bec9-125">刪除 [我的系統] 存放區中的所有 Ctl，然後將產生的存放區儲存到名為 *NewStore* 的檔案。</span><span class="sxs-lookup"><span data-stu-id="4bec9-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="4bec9-126">**certmgr.msc-del-all-ctl-s my** *NewStore*</span><span class="sxs-lookup"><span data-stu-id="4bec9-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="4bec9-127">儲存至名為 *NewCert* 的檔案，這是 [*x.509*](../secgloss/x-gly.md) 編碼憑證的憑證，其具有一般名稱 *mycert.cer*，且位於根憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="4bec9-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="4bec9-128">**certmgr.msc-put-c-n** *mycert.cer* **-s root** *NewCert .cer*</span><span class="sxs-lookup"><span data-stu-id="4bec9-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bec9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bec9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bec9-130">Certmgr.msc</span><span class="sxs-lookup"><span data-stu-id="4bec9-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
