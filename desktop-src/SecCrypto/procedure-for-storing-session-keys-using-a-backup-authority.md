---
description: 使用備份授權單位來儲存工作階段金鑰的應用程式，通常會遵循下列步驟。
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: 使用備份授權單位儲存工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319267"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="2f814-103">使用備份授權單位儲存工作階段金鑰</span><span class="sxs-lookup"><span data-stu-id="2f814-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="2f814-104">使用 [*備份授權*](../secgloss/b-gly.md) 單位來儲存工作階段金鑰的應用程式，通常會遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="2f814-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="2f814-105">**若要使用備份授權單位**</span><span class="sxs-lookup"><span data-stu-id="2f814-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="2f814-106">照常加密檔案。</span><span class="sxs-lookup"><span data-stu-id="2f814-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="2f814-107">將用來加密檔案的 [*工作階段金鑰*](../secgloss/s-gly.md) 匯出至 [*簡單的金鑰 blob*](../secgloss/s-gly.md)，並指定使用您自己的 [*金鑰交換公開金鑰*](../secgloss/k-gly.md) 來加密金鑰 blob。</span><span class="sxs-lookup"><span data-stu-id="2f814-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="2f814-108">將此金鑰 BLOB 儲存在加密的檔案中。</span><span class="sxs-lookup"><span data-stu-id="2f814-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="2f814-109">再次匯出工作階段金鑰，這次指定使用備份授權單位的公開金鑰來加密金鑰 BLOB。</span><span class="sxs-lookup"><span data-stu-id="2f814-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="2f814-110">將此金鑰 BLOB 連同金鑰的描述、序號等傳送給備份授權單位。</span><span class="sxs-lookup"><span data-stu-id="2f814-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="2f814-111">如果遺失 [*金鑰*](../secgloss/k-gly.md) 組，且可以建立金鑰擁有者的身分識別，則可以從 [*備份授權*](../secgloss/b-gly.md) 單位取出金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f814-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="2f814-112">建立身分識別的程式取決於特定備份授權單位的原則，而且不牽涉到 CryptoAPI。</span><span class="sxs-lookup"><span data-stu-id="2f814-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="2f814-113">針對建立工作階段金鑰所需的程式碼，並將該金鑰匯出至可寫入磁片檔案的 [*簡單金鑰 BLOB*](../secgloss/s-gly.md) ，請參閱 [範例 C 程式：匯出工作階段金鑰](example-c-program-exporting-a-session-key.md)。</span><span class="sxs-lookup"><span data-stu-id="2f814-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
