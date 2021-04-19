---
description: COPP 命令參考
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: COPP 命令參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972323"
---
# <a name="copp-command-reference"></a><span data-ttu-id="a5ebe-103">COPP 命令參考</span><span class="sxs-lookup"><span data-stu-id="a5ebe-103">COPP Command Reference</span></span>

<span data-ttu-id="a5ebe-104">本節說明 (COPP) 命令的經認證輸出保護通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="a5ebe-105">已定義下列命令。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-105">The following commands are defined.</span></span>



| <span data-ttu-id="a5ebe-106">命令</span><span class="sxs-lookup"><span data-stu-id="a5ebe-106">Command</span></span>              | <span data-ttu-id="a5ebe-107">GUID</span><span class="sxs-lookup"><span data-stu-id="a5ebe-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="a5ebe-108">設定保護層級</span><span class="sxs-lookup"><span data-stu-id="a5ebe-108">Set Protection Level</span></span> | <span data-ttu-id="a5ebe-109">**DXVA \_ COPPSetProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="a5ebe-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="a5ebe-110">設定信號</span><span class="sxs-lookup"><span data-stu-id="a5ebe-110">Set Signaling</span></span>        | <span data-ttu-id="a5ebe-111">**DXVA \_ COPPSetSignaling**</span><span class="sxs-lookup"><span data-stu-id="a5ebe-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="a5ebe-112">設定保護等級命令</span><span class="sxs-lookup"><span data-stu-id="a5ebe-112">Set Protection Level Command</span></span>

<span data-ttu-id="a5ebe-113">設定指定之輸出保護機制的保護層級。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="a5ebe-114">視連接器而定，可能會在相同的連接器上套用一個以上的保護機制，每個機制各有不同的設定。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="a5ebe-115">**GUID**： DXVA \_ COPPSetProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="a5ebe-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="a5ebe-116">**輸入資料**： [**DXVA \_ COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) 結構。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="a5ebe-117">設定信號命令</span><span class="sxs-lookup"><span data-stu-id="a5ebe-117">Set Signaling Command</span></span>

<span data-ttu-id="a5ebe-118">指定保護層級以外的視訊訊號相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="a5ebe-119">針對 CGMS-A，某些保護標準要求 televsion 信號包含與 CGMS-A 位相同之 VBI 波形封包內的外觀比例和其他資訊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="a5ebe-120">如果外觀比例資訊與影片串流不一致，則電視可能會顯示不良。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="a5ebe-121">應用程式可以使用此命令來指定外觀比例，讓圖形驅動程式能夠產生正確的 VBI 封包。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="a5ebe-122">如果未來的標準需要額外的信號資訊，則此命令也設計為可延伸。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="a5ebe-123">**GUID**： DXVA \_ COPPSetSignaling</span><span class="sxs-lookup"><span data-stu-id="a5ebe-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="a5ebe-124">**輸入資料**： [**DXVA \_ COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) 結構。</span><span class="sxs-lookup"><span data-stu-id="a5ebe-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5ebe-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5ebe-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ebe-126">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="a5ebe-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



