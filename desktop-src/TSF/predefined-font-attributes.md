---
title: '預先定義的字型屬性 (TsAttrid .h) '
description: 下列值會識別以 ITfCoNtext GetAppProperty 方法取得的字型屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- 預先定義的字型屬性文字服務架構
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb586258bb6eca1639121fa3b33a26ad560f00bb9b002c347a4e026a53442f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951944"
---
# <a name="predefined-font-attributes"></a>預先定義的字型屬性

下列值會識別以 [ITfCoNtext：： GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) 方法取得的字型屬性。 包含每個屬性類型的資料格式和內容。

## <a name="properties"></a>屬性



| 屬性                                                 | 描述                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **TSATTRID \_ 字型**                                       | 未使用。                                                                                                                   |
| **TSATTRID \_ 字型 \_ FaceName**                             | 包含文字字型的臉部名稱。                                                                                    |
| **TSATTRID \_ 字型 \_ SizePts**                              | 包含文字字型的點大小。                                                                                   |
| **TSATTRID \_ 字型 \_ 樣式**                                | 未使用。                                                                                                                   |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫**                     | 未使用。                                                                                                                   |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ BlinkingBackground** | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ LasVegasLights**     | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ MarchingBlackAnts**  | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ MarchingRedAnts**    | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ Shimmer**            | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ SparkleText**        | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ WipeDown**           | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 動畫 \_ WipeRight**          | 如果文字具有指定的動畫，則包含非零值，否則為零。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ BackgroundColor**               | 包含文字背景的 RGB 值。 如果文字色彩為自動，則包含0xFF000000。                          |
| **TSATTRID \_ 字型 \_ 樣式 \_ 閃爍**                         | 如果文字閃爍，則包含非零值，否則為零。                                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 粗體**                          | 如果文字為粗體，則包含非零值，否則為零。                                                             |
| **TSATTRID \_ 字型 \_ 樣式 \_ 大寫**                    | 如果文字為大寫，則包含非零值，否則為零。                                                      |
| **TSATTRID \_ 字型 \_ 樣式 \_ 色彩**                         | 包含文字色彩的 RGB 值。 如果文字色彩為自動，則包含0xFF000000。                               |
| **TSATTRID \_ 字型 \_ 樣式 \_ 浮凸**                        | 如果文字是浮凸，則包含非零值，否則為零。                                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 陰文**                       | 如果文字為陰文，則包含非零值，否則為零。                                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 高度**                        | 包含字型高度。 如需詳細資訊，請參閱 LOGFONT 結構的 **lfHeight** 成員。                       |
| **\_隱藏 TSATTRID 字型 \_ 樣式 \_**                        | 如果隱藏文字，則包含非零值，否則為零。                                                           |
| **TSATTRID \_ 字型 \_ 樣式 \_ 斜體**                        | 如果文字為斜體，則包含非零值，否則為零。                                                           |
| **TSATTRID \_ 字型 \_ 樣式 \_ 字偶間距調整**                       | 包含最小的字偶間距調整大小。 如需詳細資訊，請參閱 ITextFont：： GetKerning。                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ 小寫**                     | 如果文字是小寫，則包含非零值，否則為零。                                                        |
| **概述的 TSATTRID \_ 字型 \_ 樣式 \_**                      | 如果已加上文字，則包含非零值，否則為零。                                                         |
| **TSATTRID \_ 字型 \_ 樣式的上 \_ 劃線**                      | 如果文字是 overlined，則包含非零值，否則為零。                                                        |
| **TSATTRID \_ 字型 \_ 樣式的上 \_ 劃線 \_ 雙精度浮點數**              | 如果文字是雙 overlined，則包含非零值，否則為零。                                                 |
| **TSATTRID \_ 字型樣式的頂線 \_ \_ \_ 單一**              | 如果文字為單一 overlined，則包含非零值，否則為零。                                                 |
| **TSATTRID \_ 字型 \_ 樣式 \_ 位置**                      | 包含字型位置。                                                                                                 |
| **\_受保護的 TSATTRID 字型 \_ 樣式 \_**                     | 如果文字受到保護，則包含非零值，否則為零。                                                        |
| **TSATTRID \_ 字型 \_ 樣式 \_ 陰影**                        | 如果文字是陰影的，則包含非零值，否則為零。                                                         |
| **TSATTRID \_ 字型 \_ 樣式 \_ SmallCaps**                     | 如果文字是小寫，則包含非零值，否則為零。                                                        |
| **TSATTRID \_ 字型 \_ 樣式 \_ 間距**                       | 包含字型間距。                                                                                                  |
| **TSATTRID \_ 字型 \_ 樣式 \_ 刪除線**                 | 未使用。                                                                                                                   |
| **TSATTRID \_ 字型 \_ 樣式 \_ 刪除線 \_ 雙精度浮點數**         | 如果文字為雙刪除線，則包含非零值，否則為零。                                             |
| **TSATTRID \_ 字型 \_ 樣式 \_ 刪除線 \_ 單一**         | 如果文字為單一刪除線，則包含非零值，否則為零。                                             |
| **TSATTRID \_ 字型 \_ 樣式注 \_ 標**                     | 如果文字為注標，則包含非零值，否則為零。                                                        |
| **TSATTRID \_ 字型 \_ 樣式 \_ 上標**                   | 如果文字是上標，則包含非零值，否則為零。                                                      |
| **TSATTRID \_ 字型 \_ 樣式 \_ 底線**                     | 如果文字加上底線，則包含非零值，否則為零。                                                       |
| **TSATTRID \_ 字型 \_ 樣式 \_ 底線 \_ 雙精度浮點數**             | 如果文字是加上底線，則包含非零值，否則為零。                                                |
| **TSATTRID \_ 字型 \_ 樣式 \_ 底線 \_ 單一**             | 如果文字是加上底線，則包含非零值，否則為零。                                                |
| **TSATTRID \_ 字型 \_ 樣式 \_ 大寫**                     | 如果文字為大寫，則包含非零值，否則為零。                                                        |
| **TSATTRID \_ 字型 \_ 樣式 \_ 粗細**                        | 包含字型粗細。 如需可能值的詳細資訊，請參閱 LOGFONT 結構的 **lfWeight** 成員。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>TsAttrid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfCoNtext：： GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

