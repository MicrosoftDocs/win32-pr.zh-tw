---
description: 加密檔案系統 (EFS) 使用公開金鑰系統，在 NTFS 檔案系統磁片區上提供個別檔案的密碼編譯保護。
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: 檔案加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996944"
---
# <a name="file-encryption"></a><span data-ttu-id="1d787-103">檔案加密</span><span class="sxs-lookup"><span data-stu-id="1d787-103">File Encryption</span></span>

<span data-ttu-id="1d787-104">加密檔案系統（或 EFS）為檔案和目錄提供額外的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="1d787-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="1d787-105">它會使用公開金鑰系統，在 NTFS 檔案系統磁片區上提供個別檔案的密碼編譯保護。</span><span class="sxs-lookup"><span data-stu-id="1d787-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="1d787-106">一般而言，Windows 安全性模型提供的檔案和目錄物件存取控制，足以保護機密資訊的未經授權存取。</span><span class="sxs-lookup"><span data-stu-id="1d787-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="1d787-107">但是，如果包含敏感性資料的膝上型電腦遺失或遭竊，則該資料的安全性保護可能會受到危害。</span><span class="sxs-lookup"><span data-stu-id="1d787-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="1d787-108">加密檔案可提高安全性。</span><span class="sxs-lookup"><span data-stu-id="1d787-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="1d787-109">若要判斷檔案系統是否支援檔案和目錄的檔案加密，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式，並檢查 **FS 檔案 \_ \_ 加密** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="1d787-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="1d787-110">請注意，下列專案無法加密：</span><span class="sxs-lookup"><span data-stu-id="1d787-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="1d787-111">壓縮檔</span><span class="sxs-lookup"><span data-stu-id="1d787-111">Compressed files</span></span>
-   <span data-ttu-id="1d787-112">系統檔案</span><span class="sxs-lookup"><span data-stu-id="1d787-112">System files</span></span>
-   <span data-ttu-id="1d787-113">系統目錄</span><span class="sxs-lookup"><span data-stu-id="1d787-113">System directories</span></span>
-   <span data-ttu-id="1d787-114">根目錄</span><span class="sxs-lookup"><span data-stu-id="1d787-114">Root directories</span></span>
-   <span data-ttu-id="1d787-115">交易</span><span class="sxs-lookup"><span data-stu-id="1d787-115">Transactions</span></span>

<span data-ttu-id="1d787-116">您可以加密稀疏檔案。</span><span class="sxs-lookup"><span data-stu-id="1d787-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="1d787-117">TxF 不支援加密檔案系統 (EFS) 檔的大部分作業。</span><span class="sxs-lookup"><span data-stu-id="1d787-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="1d787-118">TxF 唯一支援的作業是讀取作業，例如 [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)。</span><span class="sxs-lookup"><span data-stu-id="1d787-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1d787-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="1d787-119">In this section</span></span>



| <span data-ttu-id="1d787-120">主題</span><span class="sxs-lookup"><span data-stu-id="1d787-120">Topic</span></span>                                                                                               | <span data-ttu-id="1d787-121">描述</span><span class="sxs-lookup"><span data-stu-id="1d787-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d787-122">處理加密的檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="1d787-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="1d787-123">標示為已加密的檔案會使用目前的加密驅動程式，以 NTFS 檔案系統進行加密。</span><span class="sxs-lookup"><span data-stu-id="1d787-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="1d787-124">加密檔案和使用者金鑰</span><span class="sxs-lookup"><span data-stu-id="1d787-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="1d787-125">列出用來建立新金鑰、將金鑰新增至加密檔案、查詢加密檔案的金鑰，以及從加密的檔案中移除金鑰的函式。</span><span class="sxs-lookup"><span data-stu-id="1d787-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="1d787-126">備份與還原加密的檔案</span><span class="sxs-lookup"><span data-stu-id="1d787-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="1d787-127">原始加密函式會啟用加密檔案的備份。</span><span class="sxs-lookup"><span data-stu-id="1d787-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="1d787-128">如需加密的詳細資訊，請參閱 [將使用者新增至加密的](adding-users-to-an-encrypted-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="1d787-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="1d787-129">如需密碼編譯的詳細資訊，請參閱 [密碼](/windows/desktop/SecCrypto/cryptography-portal)編譯。</span><span class="sxs-lookup"><span data-stu-id="1d787-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

