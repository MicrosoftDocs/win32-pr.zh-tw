---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976448"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

根據指定的位置，播放相關聯的 **Gesturing** 狀態動畫。

-   傳回 \_ [確定] 表示作業成功。 當函式傳回時， *pdwReqID* 會包含要求的識別碼。

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

指定位置的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

指定位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **GestureAt** 要求識別碼之變數的位址。

</dd> </dl>

伺服器會根據字元目前的位置和指定的位置，自動決定並播放適當的 gesturing 動畫。 使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](iagentcharacter--prepare.md) 方法，以確保在呼叫這個方法之前可以使用動畫。

 

 




