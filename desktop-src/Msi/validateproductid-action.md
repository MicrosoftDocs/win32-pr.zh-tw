---
description: ValidateProductID 動作會將 [ProductID] 屬性設定為 [完整產品識別碼]。
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: ValidateProductID 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970229"
---
# <a name="validateproductid-action"></a>ValidateProductID 動作

ValidateProductID 動作會將 [ [**ProductID**](productid.md) ] 屬性設定為 [完整產品識別碼]。

## <a name="sequence-restrictions"></a>順序限制

此動作必須在[InstallUISequence 資料表](installuisequence-table.md)中的使用者介面 wizard 之前，以及[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的[RegisterUser 動作](registeruser-action.md)之前排序。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

安裝程式會檢查 [**ProductID**](productid.md) 屬性，檢查產品是否已成功驗證。 在成功驗證之後，安裝程式會將 **ProductID** 屬性設定為完整產品識別碼。 如果已成功驗證或由其他方法設定 **ProductID** 屬性，ValidateProductID 動作不會執行任何動作。

無論產品識別碼是否有效，ValidateProductID 動作一律會傳回成功，以便在第一次執行產品時，于命令列上輸入產品識別碼。

您可以在命令列上設定 [**PIDKEY**](pidkey.md) 屬性，或使用轉換，以驗證產品識別碼，而不需要讓使用者重新輸入這項資訊。 接著，您可以在 **PIDKEY** 屬性驗證時設定 [**ProductID**](productid.md)屬性的情況下，讓要求使用者輸入產品識別碼的對話方塊顯示成為條件式。

 

 



