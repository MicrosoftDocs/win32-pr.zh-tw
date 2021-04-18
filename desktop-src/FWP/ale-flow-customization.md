---
title: ALE 流程自訂
description: 在應用層強制執行的網路篩選 (的 Windows 篩選平台的 ALE) 層 (WFP) 可透過新增具有特定分類選項的篩選準則來自訂。
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314367"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="ea1a4-103">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="ea1a4-103">ALE Flow Customization</span></span>

<span data-ttu-id="ea1a4-104">在應用層強制執行的網路篩選 (的 Windows 篩選平台的 ALE) 層 (WFP) 可透過新增具有特定分類選項的篩選準則來自訂。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="ea1a4-105">多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="ea1a4-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="ea1a4-106">若要根據輸出多播或廣播狀態來封鎖輸入流量，請新增篩選準則，以授權輸出多播和廣播流量，並將 [ [**.Fwp \_ 分類 \_ 選項] \_ 多播 \_ 狀態**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) 選項設為 [已設定為 [已設定為已設定為 [ **\_ \_ \_ 拒絕 \_ 多播 \_ 狀態**]。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="ea1a4-107">遠端對等</span><span class="sxs-lookup"><span data-stu-id="ea1a4-107">Remote Peers</span></span>

<span data-ttu-id="ea1a4-108">若要將來自不同對等的回應封包加入至相同的 ALE 流程，請新增一個篩選準則，此篩選器會將 [ [**.Fwp \_ 分類 \_ 選項 \_ 鬆散 \_ 來源 \_ 對應**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) ] 選項設定為 [ **\_ \_ \_ 啟用 \_ 鬆散 \_ 來源 \_ 對應**]。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="ea1a4-109">請參閱使用程式碼範例的 [分類選項](using-classify-options.md) 。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="ea1a4-110">ALE 流程存留期</span><span class="sxs-lookup"><span data-stu-id="ea1a4-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="ea1a4-111">若要修改 ALE 流程的閒置超時值，請加入具有 [ [**.Fwp \_ 分類 \_ 選項 \_ MCAST \_ BCAST \_ 存留期**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) 選項] 和/或 [已將 [已設定的 **\_ \_ 單播分類選項的 \_ 單播 \_ 存留期** ] 選項設定為所需閒置 timeout 值的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="ea1a4-112">請參閱 [使用分類選項](using-classify-options.md) 來取得程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="ea1a4-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea1a4-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea1a4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea1a4-114">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="ea1a4-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="ea1a4-115">ALE 層</span><span class="sxs-lookup"><span data-stu-id="ea1a4-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ea1a4-116">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="ea1a4-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="ea1a4-117">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="ea1a4-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="ea1a4-118">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="ea1a4-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ea1a4-119">使用分類選項</span><span class="sxs-lookup"><span data-stu-id="ea1a4-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




