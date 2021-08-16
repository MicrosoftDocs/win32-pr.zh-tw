---
title: 驅動程式實例
description: 驅動程式實例
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- 可安裝的驅動程式，實例
- 可安裝的驅動程式，多個實例
- 多個驅動程式實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deea546ffb7cd848993f8aac569d3624f87988b583ea47cab7bb16451cc6ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941195"
---
# <a name="driver-instances"></a>驅動程式實例

Windows 允許可安裝驅動程式的倍數實例。 系統會在每次開啟驅動程式時建立驅動程式的實例，並在關閉驅動程式時終結實例。 驅動程式實例特別適用于支援多個裝置的可安裝驅動程式，或由多個應用程式或相同應用程式多次開啟的驅動程式。

為了協助驅動程式追蹤實例，系統會在建立實例之後，使用每個驅動程式訊息傳送驅動程式實例控制碼。 因為這個控制碼可唯一識別實例，所以可安裝的驅動程式通常會將該控制碼與它們特別配置給實例的記憶體和其他資源產生關聯。

當第一個實例開啟時，系統會傳送 [**Winspool.drv \_ LOAD**](drv-load.md)、 [**Winspool.drv \_ ENABLE**](drv-enable.md)和 [**winspool.drv \_ 開啟**](drv-open.md) 的訊息至驅動程式（依該順序）。 WINSPOOL.DRV \_ LOAD 和 Winspool.drv \_ ENABLE 訊息會通知驅動程式它現在位於記憶體中，並且已啟用作業。 WINSPOOL.DRV \_ 開啟的訊息會識別實例控制碼，而且可能包含實例的設定資訊。 在後續每次開啟相同驅動程式的實例時，系統只會傳送 WINSPOOL.DRV 的 \_ 開啟訊息。

處理 WINSPOOL.DRV \_ 載入訊息時，驅動程式通常會從登錄讀取設定、設定驅動程式和任何相關聯的硬體，以及配置記憶體供驅動程式的所有實例使用。 如果驅動程式無法完成設定或配置記憶體，則會傳回零來指示系統立即從記憶體中移除驅動程式，並防止傳送任何後續的訊息。 處理 WINSPOOL.DRV \_ ENABLE 訊息時，驅動程式會準備硬體，以接收和處理 (i/o) 要求的輸入和輸出。 準備工作可能包括安裝中斷處理常式。

處理 WINSPOOL.DRV \_ OPEN 訊息時，驅動程式會配置指定的驅動程式實例所需的記憶體或資源，然後傳回非零值。 系統會在實例的後續驅動程式訊息中，使用這個非零值做為 *驅動程式識別碼* 。 驅動程式可基於任何目的使用此識別碼。 例如，某些驅動程式會針對識別碼使用記憶體控制碼，以快速存取包含指定實例相關資訊的記憶體。

許多可安裝的驅動程式都會處理 WINSPOOL.DRV OPEN 訊息的第二個參數 \_ ，提供系統和應用程式在開啟實例時傳送額外資訊給驅動程式的方法。 參數可以是單一值，也可以是包含一組值的結構位址。 處理 WINSPOOL.DRV \_ 開啟時，驅動程式會檢查參數以判斷它是否為值，並使用指定的值（如果有的話）來完成實例的建立。

每次關閉實例時，系統就會傳送 [**Winspool.drv \_ 關閉**](drv-close.md) 訊息。 與訊息一起傳送的實例控制碼會識別要關閉的實例。 當最後一個剩餘的實例關閉時，系統會傳送 WINSPOOL.DRV \_ CLOSE、 [**winspool.drv \_ DISABLE**](drv-disable.md)和 [**winspool.drv \_ FREE**](drv-free.md) 訊息（依該順序）。 WINSPOOL.DRV \_ close 訊息會指示驅動程式關閉該實例，而 Winspool.drv \_ DISABLE 和 winspool.drv \_ FREE 訊息會通知驅動程式，它現在已停用，並會立即從記憶體釋放。

處理 WINSPOOL.DRV \_ CLOSE 訊息時，驅動程式通常會釋出配置給實例的任何記憶體或資源。 處理 WINSPOOL.DRV 停用 \_ 訊息時，驅動程式會將任何硬體置於非使用中狀態，這可能包括移除中斷處理常式。 處理 WINSPOOL.DRV \_ FREE 訊息時，驅動程式會釋出任何仍配置的記憶體或資源。

不需要可安裝的驅動程式，就能支援多個實例。 驅動程式可以針對 [**Winspool.drv \_ 開啟**](drv-open.md) 的訊息傳回零，以防止建立任何實例。

 

 




