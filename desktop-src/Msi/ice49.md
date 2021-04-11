---
description: ICE49 會檢查不是 REG SZ 型別的預設登錄專案 \_ 。
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851179"
---
# <a name="ice49"></a>ICE49

ICE49 會檢查不是 **REG \_ SZ** 型別的預設登錄專案。

## <a name="result"></a>結果

如果預設登錄專案不是 **REG \_ SZ** 型別，ICE49 會張貼警告。

## <a name="example"></a>範例

ICE49 會針對所顯示的範例報告下列警告。

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

值 ' \# 123 ' 是 **DWORD** 登錄值。

登錄[表](registry-table.md) (部分) 



| 登錄 | Name | 值 |
|----------|------|-------|
| Reg1     |      | \#123 |



 

若要修正此警告，請將值變更為輸入 **REG \_ SZ**。

具有非 **REG \_ SZ** 的元件是有效的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[條件陳述式語法](conditional-statement-syntax.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



