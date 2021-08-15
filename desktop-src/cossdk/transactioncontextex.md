---
description: 建立可開始交易的泛型交易式物件。 藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: 'TransactionCoNtextEx 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 1293445e559e7ae1ddfda5cba10b17ee3f70082760d275a06a93c4f602cfac5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409988"
---
# <a name="transactioncontextex-class"></a>TransactionCoNtextEx 類別

建立可開始交易的泛型交易式物件。 藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|--------------------------------------------------------|
| CLSID      | CLSID \_ TransactionCoNtextEx                            |
| ProgID     | L "TxCTx. TransactionCoNtextEx"                          |
| 介面 | [**ITransactionCoNtextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>使用時機

非交易式用戶端會使用這個類別來開始交易。 使用這個類別的方法，用戶端可以呼叫在交易內容物件的交易界限內執行的其他 COM 物件（如果已設定為參與交易）。 根據其商務邏輯，用戶端可以明確地認可或中止交易。

**TransactionCoNtextEx** 類別限制重複使用推動交易的商務邏輯。 基於這個理由，建議您不要使用 **TransactionCoNtextEx** 類別所具現化的物件。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。

**TransactionCoNtextEx** 類別並非設計用來 Visual Basic。 請改用 [**TransactionCoNtext**](transactioncontext.md) 類別。

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

[**ITransactionCoNtextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionCoNtext**](transactioncontext.md)
</dt> </dl>

 

 




