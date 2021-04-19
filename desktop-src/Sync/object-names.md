---
description: 命名物件提供簡單的方法，讓處理常式共用物件控制碼。
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: 物件名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987697"
---
# <a name="object-names"></a>物件名稱

命名物件提供簡單的方法，讓處理常式共用物件控制碼。 在處理常式建立了命名的事件、mutex、信號或計時器物件之後，其他進程就可以使用此名稱來呼叫適當的函式 ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa)、 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw)、 [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)或 [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) 來開啟物件的控制碼。 名稱比較會區分大小寫。

事件、信號、mutex、可等候計時器、檔案對應和工作物件的名稱會共用相同的命名空間。 如果您嘗試使用其他類型的物件所使用的名稱來建立物件，則函式會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤的 \_ \_ 控制碼**。 因此，在建立命名物件時，請使用唯一名稱，並務必檢查函式傳回值中是否有重複名稱錯誤。

如果您嘗試使用相同類型的物件所使用的名稱來建立物件，則函式會成功，並將控制碼傳回至現有的物件，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回 **錯誤 \_ 已經 \_ 存在**。 例如，如果在對 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 函式的呼叫中指定的名稱與現有 mutex 物件的名稱相符，則函式會傳回現有物件的控制碼。 在此情況下，呼叫 **CreateMutex** 相當於 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) 函數的呼叫。 因此，擁有多個處理常式的相同 mutex 使用 **CreateMutex** 相當於擁有一個進程，在其他進程呼叫 **OpenMutex** 時呼叫 **CreateMutex** ，但它不需要確保先啟動建立進程。 不過，針對 mutex 物件使用這項技術時，沒有任何呼叫進程應該要求 mutex 的立即擁有權。 如果有多個處理常式要求立即擁有權，可能會很難預測哪些程式實際獲得初始擁有權。

終端機服務環境具有適用于事件、信號、mutex、可等候計時器、檔案對應物件和工作物件的全域命名空間。 此外，每個終端機服務用戶端會話對於這些物件都有自己的個別命名空間。 終端機服務用戶端進程可以使用具有「全域」或「本機」前置詞的物件名稱 \\ \\ ，在全域或會話命名空間中明確建立物件。 如需詳細資訊，請參閱 [核心物件命名空間](../termserv/kernel-object-namespaces.md)。 使用終端機服務會話來執行快速切換使用者， (每個使用者登入不同的會話) 。 核心物件名稱必須遵循針對終端機服務所述的指導方針，讓應用程式能夠支援多個使用者。

您可以在私用命名空間中建立同步處理物件。 如需詳細資訊，請參閱 [物件命名空間](object-namespaces.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用命名物件](using-named-objects.md)
</dt> </dl>

 

 
