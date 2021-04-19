---
description: 啟用內容可讓您使用 COM 物件，而不需要註冊它們。
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: 建立 Registration-Free COM 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982490"
---
# <a name="creating-registration-free-com-objects"></a>建立 Registration-Free COM 物件

啟用內容可讓您使用 COM 物件，而不需要註冊它們。 這可讓您的應用程式根據其版本而非其登錄資訊，讓多個元件具有不同的功能。 多個元件可以使用相同的 GUID 來公開相同的 COM 物件，但根據版本有不同的功能。

當應用程式從 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)要求 GUID 時，COM 會先在使用中的啟用內容中搜尋從 PROGID 到 CLSID 的對應。 當應用程式使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得實例介面指標時，COM 會在作用中的啟用內容中搜尋，以找出將裝載 CLSID 的 DLL。 如果啟用內容不包含所需的資訊，COM 就會使用一般方法在登錄中搜尋資訊。

請注意，由於啟用內容是個別執行緒的，COM 會將建立執行緒的啟用內容封送處理到主執行緒，並在主執行緒上呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 之前啟動它。 Windows 中已經有這項功能，用戶端程式代碼不需要執行任何動作來執行此作業。

裝載的元件可以匯出 COM 類別，而不需要經過登錄。 多個元件可以針對不同的 COM 物件公開相同的 ProgID，而您的裝載應用程式應該只尋找適當的啟用內容，然後使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得主控物件的介面指標。

 

 
