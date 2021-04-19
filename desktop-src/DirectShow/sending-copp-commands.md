---
description: 傳送 COPP 命令
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: 傳送 COPP 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973129"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="f4e07-103">傳送 COPP 命令</span><span class="sxs-lookup"><span data-stu-id="f4e07-103">Sending COPP Commands</span></span>

<span data-ttu-id="f4e07-104">若要傳送經認證的輸出保護通訊協定 (COPP) 命令，請填入 [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f4e07-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="f4e07-105">**guidCommandID**。</span><span class="sxs-lookup"><span data-stu-id="f4e07-105">**guidCommandID**.</span></span> <span data-ttu-id="f4e07-106">識別命令的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f4e07-106">The GUID that identifies the command.</span></span> <span data-ttu-id="f4e07-107">請參閱 COPP 命令參考。</span><span class="sxs-lookup"><span data-stu-id="f4e07-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="f4e07-108">**dwSequence**。</span><span class="sxs-lookup"><span data-stu-id="f4e07-108">**dwSequence**.</span></span> <span data-ttu-id="f4e07-109">命令的序號。</span><span class="sxs-lookup"><span data-stu-id="f4e07-109">The command sequence number.</span></span> <span data-ttu-id="f4e07-110">請在每個命令之後遞增此值。</span><span class="sxs-lookup"><span data-stu-id="f4e07-110">Increment this value after each command.</span></span> <span data-ttu-id="f4e07-111"> (在 [起始 COPP 會話](initiating-a-copp-session.md)時，此值會顯示為 **uCommandSeq** 。 ) </span><span class="sxs-lookup"><span data-stu-id="f4e07-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="f4e07-112">**cbSizeData**。</span><span class="sxs-lookup"><span data-stu-id="f4e07-112">**cbSizeData**.</span></span> <span data-ttu-id="f4e07-113">命令所需的任何資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4e07-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="f4e07-114">**CommandData**。</span><span class="sxs-lookup"><span data-stu-id="f4e07-114">**CommandData**.</span></span> <span data-ttu-id="f4e07-115">命令的資料。</span><span class="sxs-lookup"><span data-stu-id="f4e07-115">Data for the command.</span></span>

<span data-ttu-id="f4e07-116">填入此資料之後，請計算命令的 MAC：</span><span class="sxs-lookup"><span data-stu-id="f4e07-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="f4e07-117">針對在 **AMCOPPCommand** 結構的 **macKDI** 成員後面出現的資料區塊，計算 OMAC-1 標記。</span><span class="sxs-lookup"><span data-stu-id="f4e07-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="f4e07-118">將此值複製到結構的 **macKDI** 成員。</span><span class="sxs-lookup"><span data-stu-id="f4e07-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="f4e07-119">現在將結構傳遞至 [**IAMCertifiedOutputProtection：:P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) 方法。</span><span class="sxs-lookup"><span data-stu-id="f4e07-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4e07-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4e07-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e07-121">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="f4e07-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



