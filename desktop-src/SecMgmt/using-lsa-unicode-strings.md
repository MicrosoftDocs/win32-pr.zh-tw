---
description: 許多 LSA 原則函式會使用 LSA \_ UNICODE \_ 字串結構來儲存字串資訊。 此結構會儲存字串及其長度資訊。
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: 使用 LSA Unicode 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980939"
---
# <a name="using-lsa-unicode-strings"></a>使用 LSA Unicode 字串

許多 LSA 原則函式會使用 [**LSA \_ UNICODE \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構來儲存字串資訊。 此結構會儲存字串及其長度資訊。

下列程式碼會執行將 **LPWSTR** 資料轉換成 [**LSA \_ UNICODE \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構的函式：


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



