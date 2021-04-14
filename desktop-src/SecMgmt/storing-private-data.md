---
description: LSA 原則提供兩個函數，可讓您用來設定和取出私用資料。
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: 儲存私用資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386144"
---
# <a name="storing-private-data"></a>儲存私用資料

LSA 原則提供兩個函數，可讓您用來設定和取出私用資料。 這項資料會以加密字串的形式儲存在登錄中。 例如，您可以使用這些函數來儲存伺服器帳戶密碼和其他機密資訊。

呼叫 [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) 函數來儲存和加密私用資料。 如同私用 [資料物件](private-data-object.md)中所述，私用資料物件包含三種特殊類型： local、global 和 machine。 若要建立特殊物件，請將前置詞新增至傳遞給 **LsaStorePrivateData** 的索引鍵名稱： "L $" 代表本機物件，"G $" 代表全域物件，"M $" 代表電腦物件。 如果您不是建立這些特製化類型的其中一種，則不需要指定索引鍵名稱前置詞。

若要取出並解碼先前儲存的私用資料，請呼叫 [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)。 請注意，您無法取出電腦私用資料物件;只有作業系統才能抓取機器物件。

在您可以儲存或取出私用資料之前，您的應用程式必須先取得本機 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)所示範。

下列範例會建立本機私用資料物件。 請注意，函式 InitLsaString 會將 [*unicode*](/windows/desktop/SecGloss/u-gly) 字串轉換成 [**LSA \_ unicode \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構。 這個函式的程式碼會顯示在 [使用 LSA Unicode 字串](using-lsa-unicode-strings.md)中。


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)函數所儲存的資料不會受到絕對保護。 不過，金鑰具有 [*任意的存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，只允許建立者和系統管理員讀取資料。

 

 

 
