---
description: 發出原始的 AV/C 命令
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: 發出原始的 AV/C 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385651"
---
# <a name="issuing-raw-avc-commands"></a>發出原始的 AV/C 命令

[**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)、 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)和 [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader)介面的運作方式是將方法呼叫轉譯為驅動程式的命令，然後解讀驅動程式的回應，並透過 **HRESULT** 或 output 參數傳回該驅動程式。 不過，某些裝置功能可能無法透過這些方法存取。 因此，MSDV 支援將原始的 AV/C 命令傳送到裝置。

使用這項功能時，您應該記住下列幾點：

-   此命令會直接傳遞至裝置，而不會進行錯誤檢查或參數驗證。 基於這個理由，只有當 DirectShow 介面未執行您所需的功能時，您才應該發出原始的 AV/C 命令。
-   所有原始的 AV/C 命令都是同步的。 發出命令的執行緒會封鎖，直到命令返回為止。
-   一次只能指定一個命令。 處理此命令時，裝置將會拒絕任何其他命令。
-   UVC 驅動程式不支援原始的 AV/C 命令。

若要傳送 AV/C 命令，請將命令格式化為位元組陣列。 然後呼叫 [**IAMExtTransport：： GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters)。 傳入 ED \_ RAW \_ EXT \_ DEV \_ CMD 旗標、陣列大小，以及陣列。 因為此參數的原始用途是要傳回字串值，所以您必須將陣列位址轉換成 **LPOLESTR \** _ 類型。


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



陣列的內容會直接傳遞至裝置，因此您必須小心正確地將它格式化。 命令可以將裝置的目標設為 (的) 或 (磁帶或相機) 的子單位。 您可以從 [1394 貿易協會網站](https://1394ta.org)取得相關標準。

-   AV/C 數位介面命令集一般規格
-   AV/C 磁帶錄製器/播放機子單位規格

先前的說明如何格式化 AV/C 命令，並列出單位命令。 後者的規格會列出次級命令。

**GetTransportBasicParameters** 方法可能會傳回下列其中一個錯誤碼：



| 錯誤碼              | 描述                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| 錯誤 \_ 超時          | 命令逾時。                                                           |
| 錯誤 \_ 需求 \_ 未 \_ ACCEP  | 裝置未接受命令。                                           |
| \_不 \_ 支援的錯誤   | 裝置不支援此命令。                                         |
| 錯誤 \_ 要求已 \_ 中止 | 命令已中止。 Possbly 裝置已移除或發生匯流排重設。 |



 

> [!Note]  
> 這些錯誤會以 Win32 錯誤碼（而非 Hresult）的形式傳回，因此您應該直接測試這些值，而不是使用 **SUCCEEDED** 和 **FAILED** 宏。

 

如果方法傳回 S \_ OK，則會將裝置的回應複製到陣列中。 回應承載可能會比命令更大，因此您必須配置夠大的緩衝區來保存它。 承載大小上限為512個位元組。 請注意， \_ [確定] 的傳回值不一定表示裝置已成功執行命令。 應用程式必須檢查回應承載以判斷狀態。

下列範例顯示用來搜尋絕對曲目編號搜尋的命令：


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



