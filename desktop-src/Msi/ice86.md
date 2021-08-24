---
description: 如果封裝使用條件類型之資料庫資料行中的 AdminUser 屬性，ICE86 會發出警告。 封裝作者應該在條件陳述式中使用具特殊許可權的屬性。
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c96e572a99fc31fea540fa4fbaad4179d1e8f2ecadebfcd9222527ca6a4afac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894988"
---
# <a name="ice86"></a>ICE86

如果封裝使用 [條件](condition.md)類型之資料庫資料行中的 [**ADMINUSER**](adminuser.md)屬性，ICE86 會發出警告。 封裝作者應該在條件陳述式中使用具特殊 [**許可權**](privileged.md) 的屬性。

## <a name="result"></a>結果

ICE86 會張貼下列警告。



| ICE86 警告                                                                                               | 描述                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| \` \` 在資料行% s 中找到屬性% s \` \` 。 \`% s \` 在資料列% s 中。 \`具有特殊許可權 \` 的屬性通常更適合。 | 在條件欄位中使用 [**AdminUser**](adminuser.md)屬性。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



