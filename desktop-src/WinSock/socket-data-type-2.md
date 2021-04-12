---
description: 在 Winsock 應用程式中，通訊端描述項不是檔案描述項，而且必須與 Winsock 函數搭配使用。
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: 通訊端資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319803"
---
# <a name="socket-data-type"></a>通訊端資料類型

在 Winsock 應用程式中，通訊端描述項不是檔案描述項，而且必須與 Winsock 函數搭配使用。

在 UNIX 中，通訊端描述項是由標準的檔案描述項表示。 因此，UNIX 上的通訊端描述項可以傳遞給任何標準的檔案 i/o 函式 (讀取和寫入，例如) 。

此外，UNIX 中的所有控制碼（包括通訊端控制碼）都是小型的非負整數，而某些應用程式會假設這會是 true。

Windows 通訊端控制碼沒有任何限制，除了值不正確 \_ 通訊端不是有效的通訊端。 通訊端控制碼可能會採用範圍0到無效 \_ 通訊端-1 的任何值。

因為 **通訊端** 類型不帶正負號，編譯現有的原始程式碼（例如 UNIX 環境）可能會導致編譯器警告有關簽署/不帶正負號的資料類型不符。

這表示，在 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 和 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 函式傳回時，不應藉由比較傳回值與-1 來檢查錯誤，或查看值是否為負面 (UNIX) 的常見和合法方法。 相反地，應用程式應該使用在 \_ *Winsock2* 標頭檔中定義的資訊清單常數無效通訊端。 例如：

一般 BSD UNIX 樣式


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



慣用樣式


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 



