---
title: '預先定義的清單屬性 (TsAttrid) '
description: 下列值會識別以 ITfCoNtext GetAppProperty 方法取得的清單屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- 預先定義的清單屬性文字服務架構
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105384"
---
# <a name="predefined-list-attributes"></a>預先定義的清單屬性

下列值會識別以 [ITfCoNtext：： GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) 方法取得的清單屬性。 包含每個屬性類型的資料格式和內容。

## <a name="properties"></a>屬性



| 屬性                          | 描述                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| TSATTRID \_ 清單                    | 未使用。                                                                                       |
| TSATTRID \_ 清單 \_ LevelIndel        | 包含清單的索引層級。 1是最外層的層級，2是下一個層級，依此類推。 |
| TSATTRID \_ 清單 \_ 類型              | 未使用。                                                                                       |
| TSATTRID \_ 清單 \_ 類型 \_ 阿拉伯文      | 如果清單是阿拉伯文數位清單，則包含非零值，否則為零。               |
| TSATTRID \_ 清單 \_ 類型 \_ 專案符號      | 如果清單是項目符號清單，則包含非零值，否則為零。                      |
| TSATTRID \_ 清單 \_ 類型 \_ LowerLetter | 如果清單是小寫字母清單，則包含非零值，否則為零。            |
| TSATTRID \_ 清單 \_ 類型 \_ LowerRoman  | 如果清單是小寫的羅馬數字清單，則包含非零值，否則為零。       |
| TSATTRID \_ 清單 \_ 類型 \_ UpperLetter | 如果清單是大寫的字母清單，則包含非零值，否則為零。          |
| TSATTRID \_ 清單 \_ 類型 \_ UpperRoman  | 如果清單是大寫的羅馬數字清單，則包含非零值，否則為零。      |



 

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

 

