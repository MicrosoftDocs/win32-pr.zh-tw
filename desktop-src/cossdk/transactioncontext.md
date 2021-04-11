---
description: 建立可開始交易的泛型交易式物件。
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: 'TransactionCoNtext 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191004"
---
# <a name="transactioncontext-class"></a>TransactionCoNtext 類別

建立可開始交易的泛型交易式物件。 藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionCoNtext                          |
| ProgID     | L "TxCTx. TransactionCoNtext"                        |
| 介面 | [**ITransactionCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>使用時機

非交易式用戶端會使用這個類別來開始交易。 使用這個類別的方法，用戶端可以呼叫在交易內容物件的交易界限內執行的其他 COM 物件（如果已設定為參與交易）。 根據其商務邏輯，用戶端可以明確地認可或中止交易。

**TransactionCoNtext** 類別限制重複使用推動交易的商務邏輯。 基於這個理由，建議您不要使用 **TransactionCoNtext** 類別所具現化的物件。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。

若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。 您可以使用 "COMSVCSLib. TransactionCoNtext" 將 TransactionCoNtext 物件宣告為類別名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定交易](configuring-transactions.md)
</dt> <dt>

[**ITransactionCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionCoNtextEx**](transactioncontextex.md)
</dt> </dl>

 

 




