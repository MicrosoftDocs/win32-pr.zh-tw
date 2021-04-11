---
title: 撰寫驅動程式來捕獲 PPP 框架
description: 本檔說明如何開發驅動程式，以便在傳送路徑中將 PPP 框架壓縮/加密之前，或在接收路徑中解壓縮/解密之後，才能在 Windows Vista 中加以壓縮。
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023093"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a><span data-ttu-id="4a3bf-103">撰寫驅動程式來捕獲 PPP 框架</span><span class="sxs-lookup"><span data-stu-id="4a3bf-103">Writing a Driver to Capture PPP Frames</span></span>

<span data-ttu-id="4a3bf-104">當點對點通訊協定 (PPP)  (PPP) 框架透過點對點通道通訊協定傳送 (PPTP) 已開啟加密的通道，或透過使用 IPSec 進行加密的第2層通道通訊協定 (L2TP) 通道，一般的 PPP 框架捕獲公用程式只能捕獲具有加密通訊協定身分識別欄位的 PPP 框架。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-104">When Point-to-Point Protocol (PPP) frames are sent through a Point-to-Point Tunneling Protocol (PPTP) tunnel with encryption turned on, or through a Layer 2 Tunneling Protocol (L2TP) tunnel that uses IPSec for encryption, the typical PPP frame capture utility can only capture PPP frames that have an encrypted protocol identity field.</span></span> <span data-ttu-id="4a3bf-105">本檔說明如何開發驅動程式，以便在傳送路徑中將 PPP 框架壓縮/加密之前，或在接收路徑中解壓縮/解密之後，才能在 Windows Vista 中加以壓縮。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-105">This document explains how to develop a driver that can capture PPP frames in Windows Vista before they are compressed/encrypted in the send path or after they are decompressed/decrypted in the receive path.</span></span>

1.  <span data-ttu-id="4a3bf-106">撰寫 NDIS 通訊協定驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-106">Write an NDIS protocol driver.</span></span> <span data-ttu-id="4a3bf-107">如需詳細資訊，請參閱 [ndis 6.0 通訊協定驅動程式](https://msdn.microsoft.com/library/ms795570.aspx) 或 [Ndis 通訊協定驅動程式 (ndis 5.1) ](https://msdn.microsoft.com/library/ms801145.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-107">For details, see [NDIS 6.0 Protocol Drivers](https://msdn.microsoft.com/library/ms795570.aspx) or [NDIS Protocol Drivers (NDIS 5.1)](https://msdn.microsoft.com/library/ms801145.aspx).</span></span>
2.  <span data-ttu-id="4a3bf-108">安裝硬體身分識別為 "ms netmon" 的驅動程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-108">Install the driver with a hardware identity of "ms\_netmon".</span></span> <span data-ttu-id="4a3bf-109">如需有關如何使用特定硬體識別安裝驅動程式的詳細指示，請參閱 [INF 型號一節](https://msdn.microsoft.com/library/ms794357.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-109">For detailed instructions on how to install the driver with a specific hardware identity, see [INF Models Section](https://msdn.microsoft.com/library/ms794357.aspx).</span></span>
    > [!Note]  
    > <span data-ttu-id="4a3bf-110">每部 Windows Vista 電腦都只允許安裝一個具有 "ms netmon" 硬體身分識別的驅動程式實體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-110">Each Windows Vista machine permits the installation of only one driver entity that has the "ms\_netmon" hardware identity.</span></span> <span data-ttu-id="4a3bf-111">若要安裝此身分識別的其他驅動程式，必須卸載第一個驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-111">To install another driver with this identity, the first driver must be uninstalled.</span></span> <span data-ttu-id="4a3bf-112">未使用 "ms netmon" 硬體身分識別安裝的驅動程式 \_ 無法執行捕獲 PPP 框架所需的系結。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-112">A driver that is installed without using the "ms\_netmon" hardware identity cannot perform the binding needed to capture PPP frames.</span></span>

     

3.  <span data-ttu-id="4a3bf-113">通訊協定驅動程式應指定 "ndiswanbh" 作為用來捕捉 PPP 框架的系結介面。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-113">The protocol driver should specify "ndiswanbh" as the binding interface for capturing PPP frames.</span></span> <span data-ttu-id="4a3bf-114">如需詳細指示，請參閱指定系結 [介面](https://msdn.microsoft.com/library/aa937923.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-114">For detailed instructions, see [Specifying Binding Interfaces](https://msdn.microsoft.com/library/aa937923.aspx).</span></span>
4.  <span data-ttu-id="4a3bf-115">驅動程式中的 [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) 執行應該支援 "NdisMediumWan" 作為中型陣列的一部分，因此它可以使用 [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) 函式來開啟 ndiswanbh 微型埠 edge。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-115">The [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) implementation in the driver should support "NdisMediumWan" as a part of the medium array, so that it can open the ndiswanbh miniport edge using the [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) function.</span></span>
5.  <span data-ttu-id="4a3bf-116">如果呼叫[ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx)函式時的狀態為 \_ ndis \_ ，則通訊協定驅動程式應該使用旗標 ndis 封包[ \_ \_ 類型 \_ 混雜](https://msdn.microsoft.com/library/bb314089.aspx)和 ndis 封包類型，在此系結上設定[ \_ \_ \_ 所有 \_ 本機](https://msdn.microsoft.com/library/bb314089.aspx)的[OID \_ GEN \_ 目前封 \_ 包 \_ 篩選器](https://msdn.microsoft.com/library/bb314089.aspx)OID。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-116">If the [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) function is called with status NDIS\_STATUS\_SUCCESS, the protocol driver should set the [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/bb314089.aspx) OID with the flags [NDIS\_PACKET\_TYPE\_PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) and [NDIS\_PACKET\_TYPE\_ALL\_LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) over this binding.</span></span> <span data-ttu-id="4a3bf-117">完成此操作後，通訊協定驅動程式將會從其 [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) 函式中的 ppp 框架層接收已解密的 ppp 框架。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-117">Once this is done, the protocol driver will receive the decrypted PPP frames from the PPP framing layer in its [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) function.</span></span>

> [!Note]  
> <span data-ttu-id="4a3bf-118">此資訊只適用于 Windows Vista 電腦上的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4a3bf-118">This information only applies to drivers on a Windows Vista machine.</span></span>

 

 

 




