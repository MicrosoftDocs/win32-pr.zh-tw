---
title: ADSI)  (常見的錯誤
description: 所有 ADSI 特定的錯誤都具有十六進位形式的80005xxx。 下表概述最常遇到的錯誤碼。
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efcbbbce67d9928c9ecda3840f34a1cbf6faae79ca4d9fe72830a5b57881177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692192"
---
# <a name="common-errors-adsi"></a>ADSI)  (常見的錯誤

所有 ADSI 特定的錯誤都具有十六進位形式的80005xxx。 下表概述最常遇到的錯誤碼。



| ADSI hex 錯誤碼 | Description                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | 傳遞的 ADSI 路徑名稱無效。 此錯誤的結果是在系結至物件時，將不良格式的 ADsPath 傳遞給 **GetObject** 。<br/> |
| 8000500D<br/> | 屬性快取中找不到 ADSI 屬性。<br/>                                                                                 |
| 8000500E<br/> | ADSI 物件存在。 如果您嘗試建立的 ADSI 物件與現有的 ADSI 物件名稱相同，就會發生此錯誤。<br/>    |



 

如需 ADSI 錯誤碼的完整清單，請參閱 [一般 Adsi 錯誤碼](generic-adsi-error-codes.md)。

## <a name="com-errors"></a>COM 錯誤

因為 ADSI 是由 COM 物件所組成，所以會傳回標準 COM 錯誤碼。 下表列出 ADSI 程式設計中最常遇到的 COM 錯誤碼。



| COM 十六進位錯誤碼  | Description                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | 未指定的錯誤。 ADSI 無法確定 COM 物件失敗的原因。 <br/>                                  |
| 800041E4<br/> | 找不到物件。 發生此錯誤的主要原因是在系結至物件時，ADsPath 字串拼寫錯誤。<br/> |



 

如需一些可能會在 ADSI 程式設計中發生的 COM 錯誤範例，請參閱 [泛型 Com 錯誤碼](generic-com-error-codes.md) 。

## <a name="win32-errors"></a>Win32 錯誤

十六進位形式8007xxxx 的任何錯誤碼都是標準的 Win32 錯誤碼。 如果您將最後四個數字從十六進位轉換成十進位，您可以從 Windows 2000 命令列存取錯誤：

**net helpmsg <number>**

在上述命令列中，" &lt; number &gt; " 是從十六進位轉換錯誤碼的最後四個數字所取得的十進位數。 此命令列將提供更有用的 Win32 錯誤描述，這對您的腳本而言很有説明。

 

 





