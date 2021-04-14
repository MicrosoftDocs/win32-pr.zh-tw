---
title: DllSurrogate
description: 讓 DLL 伺服器在代理進程中執行。 如果指定了空字串，則會使用系統提供的代理;否則，此值會指定要使用的代理路徑。
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- DllSurrogate 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382954"
---
# <a name="dllsurrogate"></a>DllSurrogate

讓 DLL 伺服器在代理進程中執行。 如果指定了空字串，則會使用系統提供的代理;否則，此值會指定要使用的代理路徑。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定類別是要在代理程式中啟動的 DLL，以及要使用的代理程式。 若要使用系統提供的一般代理進程，請將 *路徑* 設定為空字串或 **Null**。 若要指定其他代理程式，請將 *路徑* 設定為代理的路徑。 如同 [**LocalServer32**](localserver32.md) 機碼下伺服器的路徑規格，不需要完整路徑規格。 必須撰寫代理，才能與 DCOM 服務正確地通訊，如 [撰寫自訂代理](writing-a-custom-surrogate.md)所述。

必須要有 **DllSurrogate** 值，才能在代理程式中啟用 DLL 伺服器。 啟用指的是呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)、 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)、 **CoCreateInstanceEx**、 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)、 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)。 在代理程式中執行 Dll 提供可執行檔的優點，包括錯誤隔離、同時提供多個用戶端的能力，以及允許伺服器在分散式環境中提供服務給遠端用戶端。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[DLL 代理](dll-surrogates.md)
</dt> <dt>

[**DllSurrogateExecutable**](dllsurrogateexecutable.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 