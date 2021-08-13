---
description: 使用下列選項旗標，指定安裝程式不會將輸入的值寫入至 CustomAction 資料表的目標欄位中。 若要設定選項，請將此資料表中的值加入至 CustomAction 資料表之 [類型] 欄位中的值。
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: 自訂動作隱藏目標選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adc0df477510ac7d5d6bec65025b6fed1bfd7971e6ddf35da3a7e4cbc714690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638161"
---
# <a name="custom-action-hidden-target-option"></a>自訂動作隱藏目標選項

使用下列選項旗標，指定安裝程式不會將輸入的值寫入至 [CustomAction 資料表](customaction-table.md) 的目標欄位中。 若要設定選項，請將此資料表中的值加入至 CustomAction 資料表之 [類型] 欄位中的值。



| 常數                            | 十六進位 | Decimal | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (無)                              | 0x0000      | 0       | 安裝程式可能會將 CustomAction 資料表的目標資料行中的值寫入記錄檔中。                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | 安裝程式無法將 [CustomAction 資料表](customaction-table.md) 的目標資料行中的值寫入記錄檔中。 當安裝程式執行自訂動作時，也不會記錄 CustomActionData 屬性。<br/> 因為安裝程式會從與自訂動作相同名稱的屬性中設定 CustomActionData 的值，所以該屬性必須列在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，以防止其值出現在記錄檔中。<br/> |



 

如需詳細資訊，請參閱[防止機密資訊寫入記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> <dt>

[關於自訂動作](about-custom-actions.md)
</dt> <dt>

[使用自訂動作](using-custom-actions.md)
</dt> </dl>

 

 




