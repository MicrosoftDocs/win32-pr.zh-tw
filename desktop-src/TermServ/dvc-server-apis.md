---
title: DVC 伺服器 Api
description: 動態虛擬通道 (DVC) server Api 是由連接的遠端桌面連線 (RDC) 伺服器所執行。
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382609"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="39dd6-103">DVC 伺服器 Api</span><span class="sxs-lookup"><span data-stu-id="39dd6-103">DVC Server APIs</span></span>

<span data-ttu-id="39dd6-104">動態虛擬通道 (DVC) server Api 是由連接的遠端桌面連線 (RDC) 伺服器所執行。</span><span class="sxs-lookup"><span data-stu-id="39dd6-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="39dd6-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="39dd6-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="39dd6-106">**IWTSServerChannel**</span><span class="sxs-lookup"><span data-stu-id="39dd6-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="39dd6-107">不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="39dd6-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="39dd6-108">**IWTSServerChannelManager**</span><span class="sxs-lookup"><span data-stu-id="39dd6-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="39dd6-109">不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="39dd6-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="39dd6-110">**TPriority**</span><span class="sxs-lookup"><span data-stu-id="39dd6-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="39dd6-111">不使用這個列舉型別。</span><span class="sxs-lookup"><span data-stu-id="39dd6-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="39dd6-112">其他伺服器 Api 行為的變更</span><span class="sxs-lookup"><span data-stu-id="39dd6-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="39dd6-113">伺服器 API 已使用額外的呼叫來擴充，以開啟動態虛擬通道 (DVC) 。</span><span class="sxs-lookup"><span data-stu-id="39dd6-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="39dd6-114">使用 [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) 函數進行額外的呼叫。</span><span class="sxs-lookup"><span data-stu-id="39dd6-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="39dd6-115">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="39dd6-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="39dd6-116">搭配使用此 API 與 DVC 時，它一律會在使用 [**通道 \_ PDU \_ 標頭**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)讀取的資料前面加上。</span><span class="sxs-lookup"><span data-stu-id="39dd6-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="39dd6-117">這表示任何讀取都必須完成，而且至少必須以 **通道 \_ PDU \_ 長度** 資料區塊傳遞做為輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="39dd6-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="39dd6-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="39dd6-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="39dd6-119">如果使用參數 *WTSVirtualFileHandle* 呼叫 [**WTSVIRTUALCHANNELQUERY**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)來抓取 DVC 的檔案控制代碼，就會套用相同的規則。</span><span class="sxs-lookup"><span data-stu-id="39dd6-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="39dd6-120">所有讀取都會包含 [**通道 \_ pdu \_ 標頭**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)，且讀取緩衝區必須至少為 **通道 \_ pdu \_ 長度** 的大小。</span><span class="sxs-lookup"><span data-stu-id="39dd6-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 