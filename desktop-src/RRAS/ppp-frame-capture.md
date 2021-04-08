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
# <a name="writing-a-driver-to-capture-ppp-frames"></a>撰寫驅動程式來捕獲 PPP 框架

當點對點通訊協定 (PPP)  (PPP) 框架透過點對點通道通訊協定傳送 (PPTP) 已開啟加密的通道，或透過使用 IPSec 進行加密的第2層通道通訊協定 (L2TP) 通道，一般的 PPP 框架捕獲公用程式只能捕獲具有加密通訊協定身分識別欄位的 PPP 框架。 本檔說明如何開發驅動程式，以便在傳送路徑中將 PPP 框架壓縮/加密之前，或在接收路徑中解壓縮/解密之後，才能在 Windows Vista 中加以壓縮。

1.  撰寫 NDIS 通訊協定驅動程式。 如需詳細資訊，請參閱 [ndis 6.0 通訊協定驅動程式](https://msdn.microsoft.com/library/ms795570.aspx) 或 [Ndis 通訊協定驅動程式 (ndis 5.1) ](https://msdn.microsoft.com/library/ms801145.aspx)。
2.  安裝硬體身分識別為 "ms netmon" 的驅動程式 \_ 。 如需有關如何使用特定硬體識別安裝驅動程式的詳細指示，請參閱 [INF 型號一節](https://msdn.microsoft.com/library/ms794357.aspx)。
    > [!Note]  
    > 每部 Windows Vista 電腦都只允許安裝一個具有 "ms netmon" 硬體身分識別的驅動程式實體 \_ 。 若要安裝此身分識別的其他驅動程式，必須卸載第一個驅動程式。 未使用 "ms netmon" 硬體身分識別安裝的驅動程式 \_ 無法執行捕獲 PPP 框架所需的系結。

     

3.  通訊協定驅動程式應指定 "ndiswanbh" 作為用來捕捉 PPP 框架的系結介面。 如需詳細指示，請參閱指定系結 [介面](https://msdn.microsoft.com/library/aa937923.aspx)。
4.  驅動程式中的 [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) 執行應該支援 "NdisMediumWan" 作為中型陣列的一部分，因此它可以使用 [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) 函式來開啟 ndiswanbh 微型埠 edge。
5.  如果呼叫[ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx)函式時的狀態為 \_ ndis \_ ，則通訊協定驅動程式應該使用旗標 ndis 封包[ \_ \_ 類型 \_ 混雜](https://msdn.microsoft.com/library/bb314089.aspx)和 ndis 封包類型，在此系結上設定[ \_ \_ \_ 所有 \_ 本機](https://msdn.microsoft.com/library/bb314089.aspx)的[OID \_ GEN \_ 目前封 \_ 包 \_ 篩選器](https://msdn.microsoft.com/library/bb314089.aspx)OID。 完成此操作後，通訊協定驅動程式將會從其 [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) 函式中的 ppp 框架層接收已解密的 ppp 框架。

> [!Note]  
> 此資訊只適用于 Windows Vista 電腦上的驅動程式。

 

 

 




