---
description: 列出封套資料之功能的變更。
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: 新增封包資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982370"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="fa376-103">新增封包資料</span><span class="sxs-lookup"><span data-stu-id="fa376-103">Enveloped Data Additions</span></span>

<span data-ttu-id="fa376-104">已對封包資料功能進行下列變更：</span><span class="sxs-lookup"><span data-stu-id="fa376-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="fa376-105">收件者識別不僅可以透過簽發者和序號 (PKCS \# 7 1.5) ，也可以透過金鑰識別碼來完成。</span><span class="sxs-lookup"><span data-stu-id="fa376-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="fa376-106">提供三個收件者金鑰交換選項：</span><span class="sxs-lookup"><span data-stu-id="fa376-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="fa376-107">使用 RSA 金鑰的金鑰傳輸。</span><span class="sxs-lookup"><span data-stu-id="fa376-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="fa376-108">使用 Ephemeral-Static Diffie-Hellman 以3DES 或 RC2 包裝之演算法金鑰的金鑰協定，或 Ephemeral-Static 橢圓曲線 Diffie-Hellman 以 AES 包裝的演算法金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa376-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="fa376-109">金鑰加密金鑰或郵寄清單金鑰傳送，用來加密內容加密金鑰的金鑰已發佈至收件者。</span><span class="sxs-lookup"><span data-stu-id="fa376-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="fa376-110">RC2、3DES 和 AES 可以作為金鑰包裝演算法。</span><span class="sxs-lookup"><span data-stu-id="fa376-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="fa376-111">未受保護的屬性可以包含在訊息中。</span><span class="sxs-lookup"><span data-stu-id="fa376-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="fa376-112">已新增 **OriginatorInfo** 欄位，其中包含建立者的相關資訊，其中可包含憑證和 crl。</span><span class="sxs-lookup"><span data-stu-id="fa376-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="fa376-113">橢圓曲線密碼編譯 (ECC) 演算法和 AES 需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fa376-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



