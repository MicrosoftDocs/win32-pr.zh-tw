---
title: '預先定義的文字屬性 (TsAttrid .h) '
description: 下列值會識別使用 ITfCoNtext GetAppProperty 方法取得的 text 屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- 預先定義的文字屬性文字服務架構
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105383"
---
# <a name="predefined-text-attributes"></a>預先定義的文字屬性

下列值會識別以 [**ITfCoNtext：： GetAppProperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) 方法取得的 text 屬性。 包含每個屬性類型的資料格式和內容。

## <a name="properties"></a>屬性



| 屬性                                     | 描述                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| TSATTRID \_ 文字                               | 未使用。                                                                                                                                                |
| TSATTRID \_ 文字 \_ 對齊                    | 未使用。                                                                                                                                                |
| TSATTRID \_ 文字 \_ 對齊 \_ 中心            | 如果文字是置中或為零，則包含非零值。                                                                                      |
| TSATTRID \_ 文字 \_ 對齊方式 \_ 對齊           | 如果文字是對齊的，則包含非零值，否則為零。                                                                                     |
| TSATTRID \_ 文字 \_ 靠 \_ 左對齊              | 如果文字靠左對齊，則包含非零值，否則為零。                                                                                  |
| TSATTRID \_ 文字 \_ 靠 \_ 右對齊             | 如果文字靠右對齊，則包含非零值，否則為零。                                                                                 |
| TSATTRID \_ 文字 \_ EmbeddedObject               | 如果文字是内嵌物件，則包含非零值，否則為零。                                                                            |
| TSATTRID \_ 文字 \_ 斷字                  | 如果文字以斷字元或零為零，則包含非零值。                                                                                    |
| TSATTRID \_ 文字 \_ 語言                     | 包含文字的 **LANGID** 語言識別項。                                                                                                 |
| TSATTRID \_ 文字 \_ 連結                         | 包含連結化物件的指標。 呼叫端必須使用 QueryInterface 方法來取得所需的介面，例如 **IUniformResourceLocator**。 |
| TSATTRID \_ 文字 \_ 方向                  | 指定文字基底線與裝置 X 軸之間的角度（以十分之一度為單位）。                                                          |
| TSATTRID \_ 文字 \_ 段落                         | 未使用。                                                                                                                                                |
| TSATTRID \_ 文字 \_ 段落 \_ FirstLineIndent        | 包含段落第一行縮排的點數目。                                                                            |
| TSATTRID \_ 文字 \_ 段落 \_ LeftIndent             | 包含從左邊縮排段落的點數目。                                                                              |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing            | 未使用。                                                                                                                                                |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing \_   | 包含段落行距的最小行數。                                                                              |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing \_ 雙精度浮點數    | 如果段落是雙重間距，則包含非零值，否則為零。                                                                            |
| TSATTRID \_ 精確的文字 \_ 段落 \_ LineSpacing \_   | 包含段落行距的確切行數。                                                                                |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing \_ 多重  | 包含段落多行間距的行數。                                                                             |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing \_ OnePtFive | 如果段落是1，而一個半行間距或零，則包含非零值。                                                             |
| TSATTRID \_ 文字 \_ 段落 \_ LineSpacing \_ 單一    | 如果段落為單一間距，則包含非零值，否則為零。                                                                            |
| TSATTRID \_ 文字 \_ 段落 \_ RightIndent            | 包含段落從右邊縮排的點數目。                                                                             |
| TSATTRID \_ 文字 \_ 段落 \_ SpaceAfter             | 包含段落後間距的點數。                                                                                            |
| TSATTRID \_ 文字 \_ 段落 \_ SpaceBefore            | 包含段落前間距的點數。                                                                                           |
| TSATTRID \_ 文字 \_ ReadOnly                     | 如果文字是唯讀，則為零，否則為非零。                                                                                             |
| TSATTRID \_ 文字 \_ RightToLeft                  | 如果文字是由右至左閱讀，則包含零，否則為非零。                                                                                 |
| TSATTRID \_ 文字 \_ VerticalWriting              | 指定文字是垂直或水準。 如果文字是垂直的，則包含零（如果文字是水準或非零）。                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>TsAttrid。h</dt> </dl> |



 

