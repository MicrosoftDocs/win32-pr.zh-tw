---
title: 選擇編碼方法
description: 選擇編碼方法
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- 設定檔，選擇編碼方法
- 設定檔，編碼方法
- 編解碼器，選擇編碼方法
- 編解碼器，編碼方法
- 設定檔，選取編碼方法
- 編解碼器，選取編碼方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969850"
---
# <a name="choosing-an-encoding-method"></a>選擇編碼方法

某些編解碼器（例如 Windows Media 視訊9編解碼器）支援多種編碼方法。 您為數據流選擇的編碼方法將取決於資料流程的傳遞方式。 下表說明使用各種編碼方法的時機。



| 編碼方法                | Description                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1-傳遞常數的位速率 (CBR)  | 即時串流的唯一選項。 編碼為可預測的位元速率，並提供所有編碼方法的最低品質。                                                                    |
| 2-通過 CBR                     | 針對將透過網路串流至用戶端讀取器，但不是從即時來源進行廣播的檔案使用。 編碼為可預測的位元速率，但品質優於 1-通過 CBR。 |
| 1-傳遞變數位元速率 (VBR)  | 當您需要指定編碼輸出的品質時，請使用。 提供所有編碼方法的最一致品質。 僅適用于本機檔案或供下載之用。                        |
| 2-通過 VBR –未受限制     | 當您需要指定頻寬，但可接受指定頻寬周圍的波動時，請使用。 本機檔案或僅限下載。                                                    |
| 2-通過 VBR –受限制       | 在與未受限制的情況下使用相同的情況下，但您必須指定最大的暫時位元速率。 本機檔案或僅限下載。                                                |



 

下表列出 Windows Media Format SDK 隨附的編解碼器所支援的編碼方法。



| 轉碼器                                  | Cbr | 2-通過 CBR | Vbr | 2-通過 VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media 視訊9                  | X   | X          | X   | X          |
| Windows Media 音訊9和更新版本        | X   | X          | X   | X          |
| Windows Media 視訊9螢幕           | X   |            | X   |            |
| Windows Media 音訊9語音            | X   |            |     |            |
| Windows Media 音訊專業人員       | X   | X          | X   | X          |
| Windows Media 音訊無損           |     |            | X   |            |
| Windows Media 視訊9映射和更新版本  | X   |            | X   |            |
| Windows Media 視訊 9 Advanced Profile | X   | X          | X   | X          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設計設定檔**](designing-profiles.md)
</dt> <dt>

[**固定位元速率 (CBR) 編碼**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**雙通路編碼**](two-pass-encoding.md)
</dt> <dt>

[**變數位速率 (VBR) 編碼**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




