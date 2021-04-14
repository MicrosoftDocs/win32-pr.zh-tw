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
# <a name="dvc-server-apis"></a>DVC 伺服器 Api

動態虛擬通道 (DVC) server Api 是由連接的遠端桌面連線 (RDC) 伺服器所執行。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

不支援此介面。

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

不支援此介面。

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

不使用這個列舉型別。

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>其他伺服器 Api 行為的變更

-   伺服器 API 已使用額外的呼叫來擴充，以開啟動態虛擬通道 (DVC) 。 使用 [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) 函數進行額外的呼叫。
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    搭配使用此 API 與 DVC 時，它一律會在使用 [**通道 \_ PDU \_ 標頭**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)讀取的資料前面加上。 這表示任何讀取都必須完成，而且至少必須以 **通道 \_ PDU \_ 長度** 資料區塊傳遞做為輸入緩衝區。

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    如果使用參數 *WTSVirtualFileHandle* 呼叫 [**WTSVIRTUALCHANNELQUERY**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)來抓取 DVC 的檔案控制代碼，就會套用相同的規則。 所有讀取都會包含 [**通道 \_ pdu \_ 標頭**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)，且讀取緩衝區必須至少為 **通道 \_ pdu \_ 長度** 的大小。

 

 