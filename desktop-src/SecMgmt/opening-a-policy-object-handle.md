---
description: 大部分的 LSA 原則函式都需要原則物件的控制碼，系統才能進行查詢或修改。 若要取得原則物件的控制碼，請呼叫 LsaOpenPolicy 並指定您想要存取之系統的名稱，以及所需的存取權限集。
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: 開啟原則物件控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978380"
---
# <a name="opening-a-policy-object-handle"></a>開啟原則物件控制碼

大部分的 LSA 原則函式都需要 [**原則**](policy-object.md) 物件的控制碼，系統才能進行查詢或修改。 若要取得 **原則** 物件的控制碼，請呼叫 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) 並指定您想要存取之系統的名稱，以及所需的存取權限集。

應用程式所需的存取權限取決於它所執行的動作。 如需每個函式所需許可權的詳細資訊，請參閱 [LSA 原則](management-functions.md)函式中該函數的描述。

如果呼叫 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) 成功，它會將控制碼傳回給指定系統的 [**原則**](policy-object.md) 物件。 然後，您的應用程式會在後續的 LSA 原則函式呼叫中傳遞這個控制碼。 當您的應用程式不再需要控制碼時，它應該呼叫 [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) 來釋放它。

下列範例顯示如何開啟 [**原則**](policy-object.md) 物件控制碼。


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



在上述範例中，應用程式要求原則 \_ 所有 \_ 訪問 [*許可權*](/windows/desktop/SecGloss/p-gly)。 如需您的應用程式在呼叫 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)時應要求哪些許可權的詳細資訊，請參閱應用程式將傳遞 [**原則**](policy-object.md) 物件控制碼的函式描述。

若要開啟受信任網域的 [**原則**](policy-object.md) 物件的控制碼，請呼叫 [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (建立與網域) 的新信任關係，或呼叫 [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (來存取現有的受信任網域) 。 這兩個函式都會設定 [**LSA \_ 控制碼**](lsa-handle.md)的指標，然後您可以在後續的 LSA 原則函式呼叫中指定。 如同 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)，如果您的應用程式不再需要受信任網域的 **原則** 物件的控制碼，就應該呼叫 [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) 。

 

 
