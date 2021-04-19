---
description: 使用雜湊和數位簽章函式時，使用者可以數位方式簽署資料，讓其他使用者可以確認資料在簽署後尚未變更。 也可以驗證簽署資料之使用者的身分識別。
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: 雜湊和數位簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987307"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="7863f-104">雜湊和數位簽章</span><span class="sxs-lookup"><span data-stu-id="7863f-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="7863f-105">使用 [雜湊和數位簽章](cryptography-functions.md)函式時，使用者可以數位方式簽署資料，讓其他使用者可以確認資料在簽署後尚未變更。</span><span class="sxs-lookup"><span data-stu-id="7863f-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="7863f-106">也可以驗證簽署資料之使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7863f-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="7863f-107">[*數位簽章*](../secgloss/d-gly.md)是由少量的二進位資料所組成，通常少於256個位元組。</span><span class="sxs-lookup"><span data-stu-id="7863f-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="7863f-108">此簽章可以與已簽署的訊息配套或個別儲存，視特定應用程式的執行方式而定。</span><span class="sxs-lookup"><span data-stu-id="7863f-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="7863f-109">Microsoft 強式密碼編譯提供者會建立符合 RSA [*公開金鑰加密標準*](../secgloss/p-gly.md) (PKCS) 1 的數位簽章 \# 。</span><span class="sxs-lookup"><span data-stu-id="7863f-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
