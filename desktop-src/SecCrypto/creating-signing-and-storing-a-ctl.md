---
description: 建立已簽署的憑證信任清單 (CTL) ，並將其儲存至憑證存放區。
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: 建立、簽署和儲存 CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973242"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="5fa23-103">建立、簽署和儲存 CTL</span><span class="sxs-lookup"><span data-stu-id="5fa23-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="5fa23-104">下列程式會建立已簽署的 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 並將其儲存至 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa23-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="5fa23-105">**建立和簽署 CTL**</span><span class="sxs-lookup"><span data-stu-id="5fa23-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="5fa23-106">建立要儲存在 [*CTL*](../secgloss/c-gly.md)中的專案陣列。</span><span class="sxs-lookup"><span data-stu-id="5fa23-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="5fa23-107">如果是受信任的憑證，這必須是受信任憑證的 SHA1 或 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="5fa23-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="5fa23-108">初始化 [**CTL \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) 結構，其中包含剛剛建立之專案的陣列。</span><span class="sxs-lookup"><span data-stu-id="5fa23-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="5fa23-109">將 [**CMSG \_ 簽署的 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) 結構初始化。</span><span class="sxs-lookup"><span data-stu-id="5fa23-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="5fa23-110">呼叫 [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)。</span><span class="sxs-lookup"><span data-stu-id="5fa23-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="5fa23-111">此函式呼叫會傳回 PKCS 7 格式) 的帶正負號編碼 CTL (的指標， \# 其中包含步驟1中建立的專案清單。</span><span class="sxs-lookup"><span data-stu-id="5fa23-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="5fa23-112">**將 CTL 新增至憑證存放區**</span><span class="sxs-lookup"><span data-stu-id="5fa23-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="5fa23-113">取得已簽署且已編碼之 CTL 的指標。</span><span class="sxs-lookup"><span data-stu-id="5fa23-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="5fa23-114">使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)呼叫來開啟目標憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="5fa23-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="5fa23-115">呼叫 [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)。</span><span class="sxs-lookup"><span data-stu-id="5fa23-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
