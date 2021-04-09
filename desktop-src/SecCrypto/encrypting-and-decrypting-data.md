---
description: 當檔或文字需要由單一使用者保護隱私權，或是在所有人都可以存取相同秘密密碼的一小部分人員之間共用檔時，可以完成簡單加密/解密。
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: 加密和解密資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944874"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="68a50-103">加密和解密資料</span><span class="sxs-lookup"><span data-stu-id="68a50-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="68a50-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="68a50-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="68a50-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="68a50-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="68a50-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="68a50-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="68a50-107">當檔或文字需要由單一使用者保護隱私權，或是在所有人都可以存取相同秘密密碼的一小部分人員之間共用檔時，可以完成簡單加密/解密。</span><span class="sxs-lookup"><span data-stu-id="68a50-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="68a50-108">CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 a。</span><span class="sxs-lookup"><span data-stu-id="68a50-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="68a50-109">因此，只有 CAPICOM 才能解密 CAPICOM a 物件。</span><span class="sxs-lookup"><span data-stu-id="68a50-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="68a50-110">下列各節顯示加密和解密工作的範例：</span><span class="sxs-lookup"><span data-stu-id="68a50-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="68a50-111">在 CAPICOM 中加密訊息</span><span class="sxs-lookup"><span data-stu-id="68a50-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="68a50-112">在 CAPICOM 中解密訊息</span><span class="sxs-lookup"><span data-stu-id="68a50-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



