---
description: 下列各節中的範例程式會執行需要公開/私密金鑰組才能加密和解密檔案、訊息和簽章的作業。
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: 必要的金鑰容器、金鑰和憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694951"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="8e7db-103">必要的金鑰容器、金鑰和憑證</span><span class="sxs-lookup"><span data-stu-id="8e7db-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="8e7db-104">下列各節中的範例程式會執行需要 [*公開/私密金鑰*](../secgloss/p-gly.md) 組才能加密和解密檔案、訊息和簽章的作業。</span><span class="sxs-lookup"><span data-stu-id="8e7db-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="8e7db-105">其中有許多程式會在執行時間進行編譯、連結及執行，但不會有適當的 [*金鑰容器*](../secgloss/k-gly.md)、金鑰、 [*憑證存放區*](../secgloss/c-gly.md)和憑證存在於這些存放區中。</span><span class="sxs-lookup"><span data-stu-id="8e7db-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="8e7db-106">此外，「我的存放區」中的某些憑證必須設定部分的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7db-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="8e7db-107">若要建立所需的預設金鑰容器，您可以執行 [C 程式範例中的程式：建立金鑰容器和產生金鑰](example-c-program-creating-a-key-container-and-generating-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7db-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="8e7db-108">請注意，金鑰容器的建立不會自動產生公開/私密金鑰組。</span><span class="sxs-lookup"><span data-stu-id="8e7db-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="8e7db-109">但是，範例程式會建立金鑰容器，並產生公開/私密金鑰組。</span><span class="sxs-lookup"><span data-stu-id="8e7db-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="8e7db-110">在產生公開/私密金鑰組之後，您可以從 [*憑證授權單位*](../secgloss/c-gly.md) 單位)  (CA 取得測試憑證（使用這些金鑰）。</span><span class="sxs-lookup"><span data-stu-id="8e7db-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="8e7db-111">有幾個程式假設具有特定主體名稱的憑證存在於 [我的系統] 存放區中。</span><span class="sxs-lookup"><span data-stu-id="8e7db-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="8e7db-112">尤其是，有數個程式會尋找主體名稱為 "Full Test Cert" 和 "Hortense" 的憑證。</span><span class="sxs-lookup"><span data-stu-id="8e7db-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="8e7db-113">您可以在程式碼中變更憑證的主體名稱，以符合「我的憑證存放區」中存在之憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7db-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="8e7db-114">在 [範例 C 程式中執行範例程式：列出存放區](example-c-program-listing-the-certificates-in-a-store.md) 中的憑證將會顯示存放區中的所有憑證，以及在這些憑證上設定的所有擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7db-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
