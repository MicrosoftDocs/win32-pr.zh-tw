---
description: RegisterUser 動作會向安裝程式註冊使用者資訊，以識別產品的使用者。
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626713"
---
# <a name="registeruser-action"></a>RegisterUser 動作

RegisterUser 動作會向安裝程式註冊使用者資訊，以識別產品的使用者。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述   |
|-------|------------------------------|
| \[1\] | 已註冊的使用者資訊。 |



 

## <a name="remarks"></a>備註

系統管理安裝期間不會執行 RegisterUser 動作。 如果 [ValidateProductID 動作](validateproductid-action.md)尚未驗證使用者輸入的產品識別碼，就不會設定 [**ProductID**](productid.md) 屬性，此動作不會執行任何動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用者**](username.md)
</dt> <dt>

[**名稱**](companyname.md)
</dt> <dt>

[**產品**](productid.md)
</dt> </dl>

 

 



