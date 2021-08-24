---
title: 使用會話的標記
description: 會話對會話啟用可讓用戶端進程在指定的會話上啟用本機伺服器處理常式。
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868848"
---
# <a name="using-a-session-moniker"></a>使用會話的標記

會話對會話啟用可讓用戶端進程在指定的會話上啟用本機伺服器處理常式。 您可以使用系統提供的會話標記，以每個會話為基礎來執行此動作。 如需建立會話的標記的詳細資訊，請參閱會話 [對會話啟用與會話的標記](session-to-session-activation-with-a-session-moniker.md)。

下列範例示範如何在會話識別碼為3的會話上啟用類別識別碼為 "10000013-0000-0000-0000-000000000001" 的本機伺服器處理常式。

首先，此範例會呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式來初始化 COM 程式庫。 然後，此範例會呼叫 [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) ，以取得 [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) 介面之執行的指標。 這個物件會儲存有關「標記系結」作業的資訊;需要指標才能呼叫 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 介面的方法。 接下來，此範例會呼叫 [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) 函式來建立複合會話標記，然後呼叫 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) 方法，以使用新建立的會話名字標記來啟動用戶端與伺服器進程之間的連接。 至此，您可以使用介面指標，在物件上執行所需的作業。 最後，此範例會釋放系結內容，並呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式。


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



因為 "{類別的類別識別碼（class）標記}" 也是命名類別標記的方式，所以您可以使用下列字串，將複合的標記名稱 (為類別標記所組成的會話標記) ，而不是上述範例中顯示的方式。

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> 如果相同的使用者在跨會話啟用期間登入每個會話，您可以成功地啟用任何設定為在 RunAs 互動式使用者啟用模式中執行的伺服器進程。 如果有不同的使用者登入每個會話，則伺服器必須呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式來設定適當的使用者權限，才能成功啟用，而且用戶端與伺服器之間可能會發生連接。 達成此目的的方法之一，是讓伺服器執行自訂 [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) 介面，並將實作為傳遞至 **CoInitializeSecurity**。 在任何情況下，用戶端使用者都必須具有在伺服器上執行之應用程式所指定的適當 [**啟動**](../com/launchpermission.md) 和 [**存取權限**](../com/accesspermission.md) 。 如需詳細資訊，請參閱 [COM 中的安全性](../com/security-in-com.md)。

 

For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).

 

 