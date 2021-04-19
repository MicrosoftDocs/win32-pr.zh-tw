---
description: 您可以使用 CNG 匯入和匯出對稱金鑰和非對稱金鑰。 您可以使用金鑰匯出和匯入功能，在機器之間移動金鑰。
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: 金鑰匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be59cc5f5c4b3d1a98fa30cf4e967d5469d2f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973996"
---
# <a name="key-import-and-export"></a><span data-ttu-id="88d1e-104">金鑰匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="88d1e-104">Key Import and Export</span></span>

<span data-ttu-id="88d1e-105">您可以使用 CNG 匯入和匯出 [*對稱金鑰*](/windows/desktop/SecGloss/s-gly) 和非對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="88d1e-105">You can import and export [*symmetric keys*](/windows/desktop/SecGloss/s-gly) and asymmetric keys with CNG.</span></span> <span data-ttu-id="88d1e-106">您可以使用金鑰匯出和匯入功能，在機器之間移動金鑰。</span><span class="sxs-lookup"><span data-stu-id="88d1e-106">And you can use key export and import functionality to move keys between machines.</span></span>

## <a name="symmetric-keys"></a><span data-ttu-id="88d1e-107">對稱金鑰</span><span class="sxs-lookup"><span data-stu-id="88d1e-107">Symmetric keys</span></span>

<span data-ttu-id="88d1e-108">若要匯入或匯出對稱式 (或會話) 金鑰（其中使用相同的金鑰來加密和解密部分資料），您可以使用 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 和 [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 函數。</span><span class="sxs-lookup"><span data-stu-id="88d1e-108">To import or export symmetric (or session) keys in which the same key is used to encrypt and decrypt some data, you can use the [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) and [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) functions.</span></span> <span data-ttu-id="88d1e-109">一般來說，您會先使用 **BCryptExportKey** 函式來匯出索引鍵，然後再使用 **BCryptImportKey** 函數進行匯入。</span><span class="sxs-lookup"><span data-stu-id="88d1e-109">Typically, you first export a key by using the **BCryptExportKey** function before importing by using the **BCryptImportKey** function.</span></span> <span data-ttu-id="88d1e-110">這些函式是設計用來啟用使用 *hExportKey* 和 *hImportKey* 參數加密匯出和匯入的金鑰;不過，Microsoft 對這些函式的執行不支援加密匯出和匯入的金鑰。</span><span class="sxs-lookup"><span data-stu-id="88d1e-110">The functions are designed to enable encryption of exported and imported keys by using the *hExportKey* and *hImportKey* parameters; however, the Microsoft implementation of these functions does not support encryption of exported and imported keys.</span></span>

## <a name="asymmetric-keys"></a><span data-ttu-id="88d1e-111">非對稱金鑰</span><span class="sxs-lookup"><span data-stu-id="88d1e-111">Asymmetric keys</span></span>

<span data-ttu-id="88d1e-112">若要匯入非對稱式 (或 [*公開/私*](/windows/desktop/SecGloss/p-gly) 用) 金鑰組，其中一個金鑰會用來加密，另一個則用來解密某些資料，您可以使用 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 或 [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) 函數的其中一個。</span><span class="sxs-lookup"><span data-stu-id="88d1e-112">To import asymmetric (or [*public/private*](/windows/desktop/SecGloss/p-gly)) key pairs in which one key is used to encrypt and the other is used to decrypt some data, you can use either of the [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) or [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) functions.</span></span> <span data-ttu-id="88d1e-113">CNG 提供者必須使用支援的 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly) 類型，對金鑰組進行編碼。</span><span class="sxs-lookup"><span data-stu-id="88d1e-113">A CNG provider must encode the key pair by using a supported [*key BLOB*](/windows/desktop/SecGloss/k-gly) type.</span></span> <span data-ttu-id="88d1e-114">[**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 可以用來建立編碼的金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="88d1e-114">[**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) can be used to create the encoded key BLOB.</span></span> <span data-ttu-id="88d1e-115">[CNG 結構](cng-structures.md) 描述 Microsoft 金鑰儲存提供者所支援的主要 BLOB 類型和結構。</span><span class="sxs-lookup"><span data-stu-id="88d1e-115">[CNG Structures](cng-structures.md) describes the key BLOB types and structures that Microsoft Key Storage Provider supports.</span></span>

<span data-ttu-id="88d1e-116">若要讓 [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 建立保存的金鑰組，輸入金鑰 BLOB 必須包含 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)。</span><span class="sxs-lookup"><span data-stu-id="88d1e-116">For [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) to create a persisted key pair, the input key BLOB must contain a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="88d1e-117">[*公開金鑰*](/windows/desktop/SecGloss/p-gly) 不會保存。</span><span class="sxs-lookup"><span data-stu-id="88d1e-117">[*Public keys*](/windows/desktop/SecGloss/p-gly) are not persisted.</span></span>

<span data-ttu-id="88d1e-118">金鑰名稱和匯出原則不是 [CNG 結構](cng-structures.md)中所定義之 [*BLOB*](/windows/desktop/SecGloss/b-gly)結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="88d1e-118">The key name and export policy are not part of the [*BLOB*](/windows/desktop/SecGloss/b-gly) structure defined in [CNG Structures](cng-structures.md).</span></span> <span data-ttu-id="88d1e-119">但是，如果 BLOB 的 BLOB 類型不是不透明的， (例如內部金鑰狀態) 的記憶體映射，則 BLOB 可能會包含金鑰名稱和匯出原則屬性。</span><span class="sxs-lookup"><span data-stu-id="88d1e-119">However, if a BLOB is of an opaque BLOB type (such as the memory image of an internal key state), the BLOB might contain the key name and export-policy properties.</span></span>

<span data-ttu-id="88d1e-120">下列程式說明如何使用其屬性匯入保存的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="88d1e-120">The following procedure describes how to import a persisted private key with its properties.</span></span>

<span data-ttu-id="88d1e-121">**匯入保存的金鑰**</span><span class="sxs-lookup"><span data-stu-id="88d1e-121">**To import a persisted key**</span></span>

1.  <span data-ttu-id="88d1e-122">使用 [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) 函數建立保存的金鑰。</span><span class="sxs-lookup"><span data-stu-id="88d1e-122">Create a persisted key by using the [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) function.</span></span>
2.  <span data-ttu-id="88d1e-123">使用 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) 函式，在金鑰組象上設定任何所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="88d1e-123">Set any desired properties on the key object by using the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function.</span></span>
3.  <span data-ttu-id="88d1e-124">將 [匯入金鑰 BLOB] 設定為索引鍵上的屬性，並將 BLOB 類型設定為 [屬性名稱]。</span><span class="sxs-lookup"><span data-stu-id="88d1e-124">Set the import key BLOB as a property on the key, with the BLOB type as the property name.</span></span>
4.  <span data-ttu-id="88d1e-125">使用 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) 函數完成保存的金鑰匯入。</span><span class="sxs-lookup"><span data-stu-id="88d1e-125">Finalize the persisted key import by using the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function.</span></span>

 

 
