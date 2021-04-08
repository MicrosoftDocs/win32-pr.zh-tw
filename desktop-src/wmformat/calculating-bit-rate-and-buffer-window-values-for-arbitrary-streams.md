---
title: 計算任意資料流程的位元速率和緩衝區視窗值
description: 計算任意資料流程的位元速率和緩衝區視窗值
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- 資料流程、位元速率
- 編解碼器，計算任意資料流程的位元速率
- 位元速率，計算任意資料流程
- 串流，計算任意資料流程的位元速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020874"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>計算任意資料流程的位元速率和緩衝區視窗值

針對任意資料流程類型計算適當的位元速率和緩衝區視窗不是精確的科學。 其中一個簡單的方法是設定比對資料流程大小與資料流程大小（以秒為單位）的位元速率。 例如，總共有68000位的資料流程持續20秒，可能會有每秒3400位的位元速率 (68000 位/20 秒 = 每秒3400位) 。

使用這個簡單技巧來指定位元速率的問題是，它不會考慮串流內的資料分佈。 許多任意資料流程在檔案的時間軸上依間隔包含大量的資料。 例如，影像資料流程的範例很大，但通常會在數秒內分隔。 您必須設定緩衝區視窗，以確保緩衝區不會溢位。

若要檢查緩衝區視窗，請將緩衝區 (視窗) 的位元速率 (位（以秒為單位）) 並除以1000，以取得資料流程的緩衝區大小（以位為單位）。 然後，請確定緩衝區大小夠大，足以容納資料流程中小於緩衝區視窗的樣本組合（呈現時間除外）。 如果有疑問，請將這兩個值的設定比您認為需要的值小一點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**緩衝處理內容**](buffering-content.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




